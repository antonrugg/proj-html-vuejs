<template>
  <footer>
    <FooterNavBarComponent :footerLinks="footerLinks"/>
  </footer>
</template>

<script>
import FooterNavBarComponent from '@/components/FooterNavBarComponent.vue'

export default {
  name: 'FooterComponent',
  components:{
    FooterNavBarComponent,
  },
  props: {
    footerLinks: Array,
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
