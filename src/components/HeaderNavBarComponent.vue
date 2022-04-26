<template>
  <nav>
      <ul>
        <li v-for="link in headerLinks" :key="link.id"><a href="#nowhere">{{ link.title }}</a></li>
        <li><font-awesome-icon icon="fa-solid fa-cart-shopping" /></li>
      </ul>
  </nav>
</template>

<script>
export default {
    name: 'HeaderNavBarComponent',
    props: {
      headerLinks: Array,
    }
}
</script>

<style lang="scss" scoped>
  @import '@/styles/generals.scss';

  
    
    li{
      text-transform: uppercase;
    }
  

  

</style>