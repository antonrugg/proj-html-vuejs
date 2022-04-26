<template>
  <div id="app">
    <HeaderComponent :headerLinks="headerLinks" :textSections="textSections"/>
    <MainComponent />
    <FooterComponent :footerLinks="footerLinks"/>
  </div>
</template>

<script>
import HeaderComponent from '@/components/HeaderComponent.vue'
import MainComponent from '@/components/MainComponent.vue'
import FooterComponent from '@/components/FooterComponent.vue'
//imported components

import headerLinks from '@/assets/data/header-nav'
import footerLinks from '@/assets/data/footer-nav'
import textSections from '@/assets/data/display-text'
//imported json datas


export default {
   

  name: 'App',
  data(){
    return{
      headerLinks,
      footerLinks,
      textSections,
    }
  },
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent
  }
}
</script>

<style lang="scss">
  @import '@/styles/generals.scss';
 

</style>
