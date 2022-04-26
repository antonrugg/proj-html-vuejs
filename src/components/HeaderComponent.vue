<template>
  <header>
    <div class="top-header">
      <LogoComponent />
      <HeaderNavBarComponent :headerLinks="headerLinks"/>    
    </div>

    <div class="main-header">
      <DisplayTextComponent :textSections="textSections[0]"/>
    </div>

    <div class="aside-etiquette demos">
      <font-awesome-icon icon="fa-solid fa-rectangle-list fa-2x" />
      <p>Demos</p>
    </div>
    <div class="aside-etiquette price">
      <p class="tag-price"><sup>&#36;</sup>39</p>
      <p>On Sale</p>
    </div>
  </header>
</template>

<script>
import HeaderNavBarComponent from '@/components/HeaderNavBarComponent.vue'
import LogoComponent from '@/components/LogoComponent.vue'
import DisplayTextComponent from '@/components/DisplayTextComponent.vue'

export default {
  name: 'HeaderComponent',
  components:{
    HeaderNavBarComponent,
    LogoComponent,
    DisplayTextComponent,
  },
  props: {
    headerLinks: Array,
    textSections: Array,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
   @import '@/styles/generals.scss';

header{
  background-image: url('@/assets/images/hero-header-bakery.jpg');
  background-position: top;
  background-repeat: no-repeat;
  background-size: 100vw;
  background-size: 100vh;
  background-size: cover;

    .top-header{
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-right: 0.2rem;
    }

    .main-header{
      margin: auto 5%;
    }

    .aside-etiquette{
      position: absolute;
      top: 130px;
      right: 10px;
      background-color: white;
      padding: 0.9rem 0.5rem 0.3rem 0.5rem;
      border-radius: 5px;
      -webkit-box-shadow: 1px 0px 17px 3px rgba(0,0,0,0.26); 
      box-shadow: 1px 0px 17px 3px rgba(0,0,0,0.26);
      text-align: center;
      max-width: 55px;
      min-width: 55px;
    }

    .aside-etiquette.price{
      position: absolute;
      top: 185px;
      right: 10px;
      padding: 0.5rem 0.3rem 0.3rem 0.3rem;
      margin-bottom: 2px;
      

      .tag-price{
        color: #65bc7b;
        font-size: 22px;
        padding: 0rem 0rem 0rem 0rem;
      }
    }

    .aside-etiquette > p{
      font-size: 10px;
      font-weight: 600;
      color: black;
    }
}

</style>
