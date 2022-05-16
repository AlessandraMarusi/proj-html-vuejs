<template>
  <div id="app">
    <header>
      <nav-comp/>
      <jumbo-comp/>
      <div class="imgFilter"></div>
    </header>
    <main>
      <main-comp/>
    </main>
    <footer>
      <footer-comp/>
    </footer>
  </div>
</template>

<script>
import FooterComp from './components/FooterComp.vue'
import JumboComp from './components/JumboComp.vue'
import MainComp from './components/MainComp.vue'
import NavComp from './components/NavComp.vue'

export default {
  name: 'App',
  components: {
    NavComp,
    JumboComp,
    MainComp,
    FooterComp
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
