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
        <ul class="m-0">
            <li class="m-0" v-for="(item, index) in datiNav" :key="index">
                <h5 class="m-0" v-if="item.link !== true">{{item.title}} <span class="arrowMenu">&#9660;</span></h5>
                <a v-else :href="item.url"><h5  class="m-0">{{item.title}}</h5></a>
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
                }
            }
            ul {
                display: flex;
                align-items: center;
                list-style: none;
                gap: 30px;
                padding-right: 30px;
                .arrowMenu {
                    font-size: 0.5rem;
                }
            }
            button {
                h4 {
                    text-transform: uppercase;
                }
            }
        }
    }
    
</style>