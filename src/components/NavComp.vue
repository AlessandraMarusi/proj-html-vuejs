<template>
<!-- TO DO LIST
    AGGIUNGERE DROPDOWN MENU
    AGGIUNGERE EFFETTI DI HOVER
    RENDERE RESPONSIVE
 -->
    <nav>
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
        z-index: 2;
        .myContainer {
            width: 90%;
            margin: auto;
            display: flex;
            align-items: center;
            .headerLogo{
                flex-grow: 1;
                img {
                    width: 300px;
                    cursor: pointer;
                }
            }
            .secBtn:hover {
            background-color: $btnColorThird;
            color: $txtColorBg;
            }
            .navItems {
                display: flex;
                align-items: center;
                list-style: none;
                gap: 30px;
                padding-right: 30px;
                li {
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
                .menuItem:hover .dropdownMenu {
                    opacity: 1;
                    visibility: visible;
                    top: 70%;
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
                    li {
                        padding: 5px;
                        transition: 0.5s;
                    }
                    li:hover {
                        color: $txtColorBg;
                    }
                }
            }
            button {
                h4 {
                    text-transform: uppercase;
                    font-size: 1.2rem;
                    font-weight: 900;
                }
            }
        }
    }
    
</style>