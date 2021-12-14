<template>
  <div id="app">
    <!-- header logo, nav, icons -->
    <Header :navLinkList="navLinks"/>

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
  data(){
    return {
      navLinks: [
        {
          name: 'home',
          isActive: false,
          isDropDown: false,
          href: '#'
        },
        {
          name: 'landing',
          isActive: true,
          isDropDown: true,
          href: '#'
        },
        {
          name: 'pages',
          isActive: false,
          isDropDown: true,
          href: '#'
        },
        {
          name: 'docs',
          isActive: false,
          isDropDown: true,
          href: '#'
        },
      ]
    }
  },
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
