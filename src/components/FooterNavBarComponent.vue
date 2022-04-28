<template>
  <nav>
    <ul>
        <li v-for="link in footerLinks" :key="link.id"><a href="#nowhere">{{ link.title }}</a></li>
        <li><a href="#nowhere"><font-awesome-icon icon="fa-solid fa-cart-shopping" /></a><span class="cart">0</span></li>
      </ul>
  </nav>
</template>

<script>
export default {
    name: 'FooterNavBarComponent',
    props: {
    footerLinks: Array,
  }
}
</script>

<style lang="scss" scoped>
  li{
    padding-top: 2.5rem;
    padding-left: 1rem;
    font-size: 11px;
    font-weight: 500;

    span{
      margin-left: 0.5rem;
      padding: 0.3rem;
      background-color: lightgray;
      border-radius: 45%;
    }
  }

</style>