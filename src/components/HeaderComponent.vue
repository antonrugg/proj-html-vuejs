<template>
  <header>
    <div class="top-header">
      <LogoComponent />
      <HeaderNavBarComponent :headerLinks="headerLinks"/>    
    </div>

    <div class="main-header" :textSections="textSections">
      <section>
        <p class="over-title">{{ textSections[0].overTitle }}</p>
        <p class="title">{{ textSections[0].title }}</p>
        <p class="text">{{ textSections[0].text }}</p>
        <button class="btn btn-header"> {{ textSections[0].buttonText }} </button>
      </section>
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


export default {
  name: 'HeaderComponent',
  components:{
    HeaderNavBarComponent,
    LogoComponent,
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

    section{
        padding: 9rem 0rem 13rem 0rem;
        width: 30%;

        p{
            padding: 0.7rem 0rem;
        }

        .over-title{
                font-size: 9px;
                font-weight: 700;
                text-transform: uppercase;
                color: $sub-title-text-color;
            }

        .title{
            font-size: 44px;
            font-weight: bold;
            color: $title-text-color;
            font-family: serif;
        }

        .title-main{
            font-size: 20px;
        }
        
        .text{
            font-size: 14px;
            font-weight: 500;
            color: $sub-title-text-color;
            width: 90%;
            line-height: 1.6;
            word-spacing: 1px;
        }

        .btn{
            background-color: white;
            padding: 0.7rem 1.4rem;
            border: none;
            border-radius: 0.3rem;
            color: $navbar-text-color;
            font-size: 11px;
            font-weight: 600;
            margin-top: 0.8rem;
            cursor: pointer;
        }

      .btn-header{
        transition: 0.3s ease;

        &:hover{
          background-color: $title-text-color;
          color: white;
          transition: 0.3s ease;
        }
      }
        
    }
}

</style>
