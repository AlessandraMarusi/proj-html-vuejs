<template>
    <section class="events">
        <div class="myContainer">
            <img class="icon" src="../assets/img/upcoming-events-calendar-icon.png" alt="Icona calendario">
            <h2>Upcoming Events</h2>
            <div class="container">
                <div class="row gx-4">
                    <event-card-comp :item="item" v-for="(item, index) in datiEvents" :key="index"/>
                </div>
            </div>
            <button class="secBtn bigBtn">View All</button>
        </div>
        <img src="../assets/svg/svg-1.svg" alt="">
    </section>
</template>

<script>
import data from '../dati.json'
import EventCardComp from './EventCardComp.vue'
export default {
  components: { EventCardComp },
    name: "EventsSection",
    data(){
        return{
            datiEvents: data.eventItems
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.events {
    background-color: $bgColor;
    .myContainer {
        width: 70%;
        margin: 0 auto;
        text-align: center;
        h2{
            color: $txtColorOnBg;
        }
    }
}
</style>