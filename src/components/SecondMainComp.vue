<template>
<!-- TO DO
CREARE UN CAROUSEL CON LE CARDS
 -->
    <section>
        <div class="myContainer">
            <div class="txtContainer">
                <h2>Faculties available ad EduPrime</h2>
                <p>A single university with load of courses, tailored to satisfy any student's needs.</p>
            </div>
            <div class="cardsContainer">
                <div class="placeholderCard"></div>
                <second-comp-cards :item="item" v-for="(item, index) in datiCard" :key="index" @activeIndex="getActiveId"/>
                <div class="placeholderCard"></div>
            </div>
        </div>
        <second-comp-infos :datiCard="datiCard" :activeId="activeId" />
        <img src="../assets/svg/svg-0.svg" alt="">
    </section>
</template>

<script>
import data from '../dati.json'
import SecondCompCards from './SecondCompCards.vue'
import SecondCompInfos from './SecondCompInfos.vue'
export default {
  components: { SecondCompCards, SecondCompInfos },
    name: "SecondMainComp",
    props:[],
        data(){
            return{
                datiCard: data.secondSectionItems,
                activeId: 0
            }
        },
    methods:{
        getActiveId(value){
            this.datiCard[this.activeId].isActive = false
            this.activeId = value - 1
            this.datiCard[this.activeId].isActive = true
            console.log(value)
        },
    }
}
</script>

<style lang="scss" scoped>
@import "../style/general";
section {
        overflow: hidden;
    /* img {
        position: absolute;
        bottom: 0%;
        left: 0%;
    } */
}
.myContainer {
    text-align: center;
    width: 100%;
    .txtContainer {
        width: 70%;
        margin: 0 auto;
        p {
            width: 30%;
            margin: 0 auto;
            padding: 25px 0;
        }
    }
    .cardsContainer {
        width: 100%;
        display: flex;
        padding: 25px 0;
        .placeholderCard {
            width: calc(100% / 7);
            box-shadow: 0px 0px 1px 0px #646464;
        }
    }
}
</style>