<template>
  <div id="app">
    <!-- header logo, nav, icons -->
    <Header />

    <!-- jumbotron -->
    <Jumbotron />  

    <!-- main -->
      <!-- sect key features -->
      <!-- sect quickstart -->
      <!-- sect build tools -->
      <!-- sect plans -->
      <!-- sect newsletter -->
    <!-- footer social, links, newsletter -->
    <!-- footer bot -->
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron
  }
}
</script>

<style lang="scss">
@import './assets/style/generals.scss';
@import './assets/style/vars.scss';


</style>
