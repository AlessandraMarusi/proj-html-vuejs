<template>
  <div id="app">
    <nav-comp/>
    <jumbo-comp/>
    <main-comp/>
    <footer-comp/>
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
@import "./style/general"

</style>
