<template>
  <section>
    <div class="card-carousel">
      <a href="#nowhere" @click="showPrev" @mouseover="pauseCarousel()" @mouseleave="playCarousel()">
        <div class="chevron left-chevron">
          <font-awesome-icon icon="fa-solid fa-chevron-left" />
        </div>
      </a>
      <!-- //chevron left -->

      <a href="#nowhere" @click="showNext" @mouseover="pauseCarousel()" @mouseleave="playCarousel()">
        <div class="chevron right-chevron">
          <font-awesome-icon icon="fa-solid fa-chevron-right" />
        </div>
      </a>
      <!-- chevron right -->
      <!-- @mouseleave="isHover = false" -->
      <div
        class="card-container"
        @mouseover="showInfos(index)"
        @mouseout="playCarousel()"
        @mouseleave="currentlyShowing = null"
        v-for="(carouselItem, index) in carouselItems.slice(min, max)"
        :key="carouselItem.id + index"
      >
        <!-- card container for loop, data in carousel.json -->
        <!-- taking just first two products with slice method -->

        <div class="product-layer" v-if="currentlyShowing === index"></div>
        <!-- layer toggle added when on hover -->

        <img
          :src="require(`@/assets/images/${carouselItem.src}-400x510.jpg`)"
          alt="choco chip cookies"
        />
        <!-- visible on hover -->
        <div class="hover-text" v-if="currentlyShowing === index">
          <h3>{{ carouselItem.title }}</h3>
          <p>{{ carouselItem.underText }}</p>
          <div>
            <span>{{ carouselItem.lowerPrice }}</span>
            <span>{{ carouselItem.higherPrice }}</span>
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
  },
  data() {
    return {
      currentlyShowing: null,
      activeProductIndex: 0,
      min: 0,
      max: 2,
    };
  },
  mounted: function () {
        this.playCarousel()
    },
  methods: {
    //function to single out hover on card
    showInfos: function (index) {
      this.currentlyShowing = index;
      this.pauseCarousel();
    },
    showPrev() {
      //function that fires on click of chevron left, to slide across products, decrement slice.method variables
      if (this.min > 0) {
        this.min = this.min - 1;
        this.max = this.max - 1;
      } else {
        this.min = this.carouselItems.length - 2;
        // console.log('min',this.min);
        this.max = this.carouselItems.length;
        // console.log('max', this.max);
      }
    },
    showNext() {
      //function that fires on click of chevron left, to slide across products, increment slice.method variables
      if (this.max === this.carouselItems.length) {
        this.min = 0;
        this.max = 2;
      } else {
        this.min = this.min + 1;
        this.max = this.max + 1;
      }
    },
     playCarousel(){
            this.interval = setInterval(() => { this.showNext() }, 3000)
        },
      pauseCarousel() {
        clearInterval(this.interval)
      },
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
  left: 15px;
}

.right-chevron {
  right: 0px;
}

.card-carousel {
  display: flex;
  margin-left: 2rem;
  position: relative;
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

.hover-text {
  position: absolute;
  z-index: 2;
  left: 30%;
  right: 20%;
  top: 40%;
  bottom: -50%;
  color: white;

  h3 {
    font-family: serif;
    font-size: 22px;
    font-weight: 700;
    width: 120%;
  }

  p {
    padding: 0.5rem 0rem 1rem 0rem;
    text-align: center;
    font-size: 10px;
  }

  span {
    font-size: 20px;
    text-align: center;
    padding-right: 0.8rem;
    padding-left: 1rem;
  }
}

.product-layer {
  height: 100%;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.3);
  position: absolute;
  top: 0;
  left: 0;
}
</style>