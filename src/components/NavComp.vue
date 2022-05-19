<template>
<!-- TO DO LIST
    AGGIUNGERE DROPDOWN MENU
    AGGIUNGERE EFFETTI DI HOVER
    RENDERE RESPONSIVE
 -->
    <nav id="navBar">
        <div class="myContainer">
            <div class="headerLogo">
                <img src="../assets/img/theme_eduprime_logo.png" alt="Edu prime logo"> 
            </div>
            <ul class="m-0 navItems">
                <li class="m-0" :class="{menuItem :! item.link}" v-for="(item, index) in datiNav" :key="index">
                    <a class="menuLink" v-if="item.link !== true">{{item.title}} <span class="arrowMenu">&#9660;</span></a>
                    <a v-else :href="item.url">{{item.title}}</a>
                    <ul class="dropdownMenu">
                        <li v-for="(dropdownItem, index) in item.menuItems" :key="index">{{dropdownItem.txt}}</li>
                    </ul>
                </li>
            </ul>
            <button class="secBtn bigBtn m-0" @click="checkApp"><a href="#"><h4 class="m-0">View Courses</h4></a></button>
        </div>
    </nav>
</template>

<script>
import data from '../dati.json'
export default {
    name: 'NavComp',
    data(){
        return{
            datiNav: data.navItems
        }
    },
    methods:{
        checkApp(){
            console.log(this.datiNav)
        }
    },
    
}
</script>

<style lang="scss" scoped>
@import "../style/general";
    nav {
        position: relative;
        height: 150px;
        color: $txtColorOnBg;
        display: flex;
        z-index: 999;
        .myContainer {
            width: 95%;
            margin: auto;
            display: flex;
            gap: 25px 0;
            /* align-items: center; */
            .headerLogo{
                width: 15%;
                display: flex;
                align-items: center;
                img {
                    width: 100%;
                    cursor: pointer;
                }
            }
            .secBtn:hover {
            background-color: $btnColorThird;
            color: $txtColorBg;
            }
            .navItems {
                flex-grow: 2;
                display: flex;
                align-items: center;
                justify-content: flex-end;
                list-style: none;
                gap: 30px;
                padding-right: 30px;
                li {
                    display: flex;
                    align-items: center;
                    height: 100%;
                    cursor: pointer;
                    a {
                        font-weight: 900;
                        font-size: 1.1rem;
                        
                    }
                }
                .arrowMenu {
                    font-size: 0.5rem;
                }
                a:hover{
                    color: $txtColorHover;
                }
                .dropdownMenu{
                    color: $titleColor;
                    border-radius: 10px;
                    text-align: left;
                    font-weight: 900;
                    opacity: 0;
                    position: absolute;
                    background: #fff;
                    width: 200px;
                    top: 120%;
                    transition: all 250ms ease-in-out;
                    -webkit-transition: all 250ms ease-in-out;
                    visibility: hidden;
                    padding: 15px;
                    box-shadow: 0 0 20px rgb(67 73 89 / 10%);
                    -webkit-box-shadow: 0 0 20px rgb(67 73 89 / 10%);
                    list-style: none;
                    z-index: 999999;
                    li {
                        padding: 5px;
                        transition: 0.5s;
                    }
                    li:hover {
                        color: $txtColorBg;
                    }
                }
                .menuItem:hover .dropdownMenu, .dropdownMenu:hover, .dropdownMenu:focus {
                    opacity: 1;
                    visibility: visible;
                    top: 70%;
                }
                /* .dropdownMenu:hover {
                    opacity: 1;
                    visibility: visible;
                    top: 70%;
                } */
            }
            button {
                h4 {
                    text-transform: uppercase;
                    font-size: 1rem;
                    font-weight: 900;
                }
            }
        }
    }
    /* On screens that are 992px or less, set the background color to blue */
    @media screen and (max-width: 1200px) {
        .myContainer {
            flex-wrap: wrap;
            justify-content: center;
        }
    }

    
</style>