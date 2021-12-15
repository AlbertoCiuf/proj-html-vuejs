<template>
  <div id="app">
    <!-- header logo, nav, icons -->
    <Header :navLinkList="navLinks"/>

    <!-- jumbotron -->
    <Jumbotron />  

    <!-- main -->
    <Main />
    
    <!-- footer -->
    <Footer 
      :companyLinks="footerCompanyLinks"
      :usefulLinks="footerUsefulLinks"
    />  
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

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
      ],
      footerCompanyLinks: [
        {
          name:'About us',
          href:'#'
        },
        {
          name:'Services',
          href:'#'
        },
        {
          name:'Team',
          href:'#'
        },
        {
          name:'Pricing',
          href:'#'
        },
        {
          name:'Project',
          href:'#'
        },
        {
          name:'Careers',
          href:'#'
        },
        {
          name:'Blog',
          href:'#'
        },
        {
          name:'Login',
          href:'#'
        },
      ],
      footerUsefulLinks: [
        {
          name:'Terms of Services',
          href:'#'
        },
        {
          name:'Privacy Policy',
          href:'#'
        },
        {
          name:'Documentation',
          href:'#'
        },
        {
          name:'Changelog',
          href:'#'
        },
        {
          name:'Components',
          href:'#'
        },
      ]
    }
  },
  components: {
    Header,
    Jumbotron,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import './assets/style/generals.scss';
@import './assets/style/vars.scss';


</style>
