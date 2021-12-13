<template>
  <div id="app">
    <!-- header logo, nav, icons -->
    <Header />

    <!-- jumbotron -->
    <Jumbotron />  

    <!-- main -->
    <Main />
      
    <!-- footer social, links, newsletter -->
    <!-- footer bot -->
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main
  }
}
</script>

<style lang="scss">
@import './assets/style/generals.scss';
@import './assets/style/vars.scss';


</style>
