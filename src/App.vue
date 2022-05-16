<template>
  <div id="app">
    <header>
      <nav-comp/>
      <jumbo-comp/>
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
@import "./style/general"

</style>
