<template>
  <div id="app">
    <HeaderComponent :headerLinks="headerLinks" />
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
//imported json datas


export default {
   

  name: 'App',
  data(){
    return{
      headerLinks,
      footerLinks
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
