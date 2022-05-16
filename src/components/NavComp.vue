<template>
    <nav>
        <img src="../assets/img/theme_eduprime_logo.png" alt="Edu prime logo"> 
        <ul>
            <li v-for="(item, index) in datiNav" :key="index">
                <h2>{{item.title}}</h2>
            </li>
        </ul>
        <button @click="checkApp">Check</button>
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

<style lang="scss">
@import "../style/general";
    nav {
        background-color: $bgColor;
    }
    
</style>