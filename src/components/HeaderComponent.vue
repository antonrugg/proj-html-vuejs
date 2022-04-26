<template>
  <header>
    <div class="top-header">
      <div class="logo-header">
        <a href="#nowhere"><img src="..\src\assets\images\avada-bakery-logo.png" alt="logo bakery"></a>
      </div>
      
      <HeaderNavBarComponent :headerLinks="headerLinks"/>
      
      
    </div>
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

header{
  background-image: url('@/assets/images/hero-header-bakery.jpg');

    .top-header{
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-right: 2rem;

      .logo-header{
        padding-top: 0.5rem;
        padding-left: 0.3rem;
      }
    }
}

</style>
