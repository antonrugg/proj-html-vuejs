<template>
  <header>
    
    <HeaderNavBarComponent :headerLinks="headerLinks"/>
  </header>
</template>

<script>
import HeaderNavBarComponent from '@/components/HeaderNavBarComponent.vue'

export default {
  name: 'HeaderComponent',
  components:{
    HeaderNavBarComponent
  },
  props: {
    headerLinks: Array,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
