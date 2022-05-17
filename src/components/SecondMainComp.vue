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
                <second-comp-cards :item="item" v-for="(item, index) in datiCard" :key="index"/>
                <div class="placeholderCard"></div>
            </div>
        </div>
        <second-comp-infos/>
    </section>
</template>

<script>
import data from '../dati.json'
import SecondCompCards from './SecondCompCards.vue'
import SecondCompInfos from './SecondCompInfos.vue'
export default {
  components: { SecondCompCards, SecondCompInfos },
    name: "SecondMainComp",
    data(){
        return{
            datiCard: data.secondSectionItems
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../style/general";
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