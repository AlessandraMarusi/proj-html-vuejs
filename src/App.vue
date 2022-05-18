<template>
  <div id="app">
    <header>
      <nav-comp/>
      <jumbo-comp/>
      <div class="imgFilter"></div>
    </header>
    <main>
      <first-main-comp/>
      <second-main-comp/>
      <timeline-comp/>
      <events-comp/>
      <courses-comp/>
      <info-comp/>
      <subscribe-bar-comp/>
      <partners-comp/>
    </main>
    <footer>
      <footer-comp/>
    </footer>
  </div>
</template>

<script>
import CoursesComp from './components/CoursesComp.vue'
import EventsComp from './components/EventsComp.vue'
import FirstMainComp from './components/FirstMainComp.vue'
import FooterComp from './components/FooterComp.vue'
import InfoComp from './components/InfoComp.vue'
import JumboComp from './components/JumboComp.vue'
import NavComp from './components/NavComp.vue'
import PartnersComp from './components/PartnersComp.vue'
import SecondMainComp from './components/SecondMainComp.vue'
import SubscribeBarComp from './components/SubscribeBarComp.vue'
import TimelineComp from './components/TimelineComp.vue'

export default {
  name: 'App',
  components: {
    NavComp,
    JumboComp,
    FooterComp,
    FirstMainComp,
    SecondMainComp,
    TimelineComp,
    EventsComp,
    CoursesComp,
    InfoComp,
    SubscribeBarComp,
    PartnersComp
  }
}
</script>

<style lang="scss">
@import "./style/general";
header {
  background-image: url("./assets/img/theme_slider2_bg-1.jpg");
  position: relative;
  .imgFilter {
    background-color: $bgColor;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0%;
    left: 0%;
    opacity: 90%;
  }
}
</style>
