<template>
  <section>
    <div class="card-carousel">
      <!-- <img :src="'@/assets/images/' + carouselItem.src" alt=""> -->
      <div class="card-container"
            @mouseover="isHover = true"
            @mouseleave="isHover = false">
            <div class="product-layer" v-show="isHover"></div>
        <a href="#nowhere"><div class="chevron left-chevron">
            <font-awesome-icon icon="fa-solid fa-chevron-left" /></div></a>
        <img
          src="@/assets/images/choco-chip-cookies-400x510.jpg"
          alt="choco chip cookies"/>
          <div class="hover-text" v-show="isHover">
              
              <h3>Choco Chip Cookies</h3>
              <p>Cookies, Pastries</p>
              <div>
                  <span>$19.00</span>
                  <span>$39.00</span>
              </div>
          </div>
      </div>

      <div class="card-container"
            @mouseover="isHover = true"
            @mouseleave="isHover = false">
             
        
        <div class="product-layer" v-show="isHover"></div>
        <a href="#nowhere"><div class="chevron right-chevron">
            <font-awesome-icon icon="fa-solid fa-chevron-right" /></div></a>
          
        <img
          src="@/assets/images/strawberry-jam-cookies-400x510.jpg"
          alt="strawberyy jam cookies"/>
        
          <div class="hover-text" v-show="isHover">
              
              <h3>Strawberyy Jam Cookies</h3>
              <p>Cookies, Pastries</p>
              <div>
                  <span>$15.00</span>
                  <span>$32.00</span>
              </div>
          </div>
         
        

      </div>
    </div>
  </section>
</template>

<script>
    

export default {
    

  name: "CarouselComponent",
  props: {
    carouselItems: Array,
    carouselItem: Object,
  },
  data(){
      return{
          isHover: false,
      }
  },
  methods: {

  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/generals.scss";

.chevron {
  position: absolute;
  top: 225px;
  background-color: #a691b2;
  height: 70px;
  width: 35px;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 5;
}

.left-chevron {
  left: 0px;
}

.right-chevron {
  right: 0px;
}

.card-carousel {
  display: flex;
  margin-left: 2rem;
  .card-container {
    position: relative;
    margin-left: 1rem;
    cursor: pointer;
  }
}

.fa-chevron-left {
  color: aliceblue;
}

.fa-chevron-right {
  color: aliceblue;
}

.hover-text{
    position: absolute;
    z-index: 2;
    left: 30%;
    right: 20%;
    top: 40%;
    bottom: -50%;
    color: white;

    h3{
        font-family: serif;
        font-size: 22px;
        font-weight: 700;
    }

    p{
        padding: 0.5rem 0rem 1rem 0rem;
        text-align: center;
        font-size: 10px;
    }

    span{
        font-size: 20px;
        text-align: center;
        padding-right: 0.8rem;
        padding-left: 1rem;
    }

    
}

.product-layer{
        height: 100%;
        width: 100%;
        background-color: rgba(0, 0, 0, 0.3);
        position: absolute;
        top: 0;
        left: 0;
    }
</style>