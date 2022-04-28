<template>
  <section class="shopping">
    <div class="text-shopping">
      <p class="over-title">{{ textSections[2].overTitle }}</p>
      <p class="title-main">{{ textSections[2].title }}</p>
      <p class="text">{{ textSections[2].text }}</p>
      <button class="btn btn-main">{{ textSections[2].buttonText }}</button>
    </div>

    <div class="products-carousel">
      <a href="#nowhere"
        ><div class="chevron right-chevron" @click="showNext">
          <font-awesome-icon icon="fa-solid fa-chevron-right" /></div
      ></a>
      <a href="#nowhere"
        ><div class="chevron left-chevron" @click="showPrev">
          <font-awesome-icon icon="fa-solid fa-chevron-left" /></div
      ></a>
      <div
        class="card"
        v-for="(product, index) in products.slice(min, max)"
        :key="product.id + index"
        @mouseover="showInfos(index)"
        @mouseleave="currentlyShowing = null"
      >
        <div class="img-container">
          <div class="product-layer" v-if="currentlyShowing === index"></div>
          <!-- layer toggle added when on hover -->

          <img
            :src="require(`@/assets/images/${product.name}-200x255.jpg`)"
            :alt="product.name"
          />
        </div>
        <div class="hover-text" v-if="currentlyShowing === index">
          <span>select options / quick view</span>
        </div>
        <div class="product-text">
          <p class="product-title">{{ product.title }}</p>
          <div>
            <p class="product-prices">{{ product.prices }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ProductsShopComponent",
  props: {
    textSections: Array,
  },
  data() {
    return {
      products: [
        {
          name: "choco-chip-cookies",
          title: "Choco Chip Cookies",
          prices: "$19.00 - $39.00",
          id: 1,
        },
        {
          name: "strawberry-jam-cookies",
          title: "Strawberry Jam Cookies",
          prices: "$24.00 - $62.00",
          id: 2,
        },
        {
          name: "strawberry-donut",
          title: "Strawberry Donut",
          prices: "$24.00 - $42.00",
          id: 3,
        },
        {
          name: "perfect-macarons",
          title: "Perfect Macarons",
          prices: "$18.00 - $52.00",
          id: 4,
        },
        {
          name: "small-cupcake",
          title: "Small Cupcake",
          prices: "$10.00 - $20.00",
          id: 5,
        },
        {
          name: "home-bread",
          title: "Home Bread",
          prices: "$7.00 - $12.00",
          id: 6,
        },
        {
          name: "glazed-pancake-with-lemon",
          title: "Glaze Pancake",
          prices: "$5.00 - $8.00",
          id: 7,
        },
        {
          name: "cookies-with-ice-cream",
          title: "Cookies with Icre cream",
          prices: "$2.00 - $5.00",
          id: 8,
        },
        {
          name: "cherry-cake",
          title: "Cherry Cake",
          prices: "$21.00 - $27.00",
          id: 9,
        },
      ],
      currentlyShowing: null,
      min: 0,
      max: 4,
    };
  },
  methods: {
    showInfos: function (index) {
      this.currentlyShowing = index;
    },
    showPrev() {
      //function that fires on click of chevron left, to slide across products, decrement slice.method variables
      if (this.min > 0) {
        this.min = this.min - 1;
        this.max = this.max - 1;
      } else {
        this.min = this.products.length - 4;
        // console.log('min',this.min);
        this.max = this.products.length;
        // console.log('max', this.max);
      }
    },
    showNext() {
      //function that fires on click of chevron left, to slide across products, increment slice.method variables
      if (this.max === this.products.length) {
        this.min = 0;
        this.max = 4;
      } else {
        this.min = this.min + 1;
        this.max = this.max + 1;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/generals.scss";

.text-shopping {
  display: flex;
  flex-direction: column;
  width: 30%;
  align-items: center;
  text-align: center;
}

.shopping {
  padding-top: 8rem;
  display: flex;
  justify-content: space-between;
  margin: auto 5%;
  padding-bottom: 10rem;

  p {
    padding: 0.7rem 0rem;
  }

  .title-main {
    font-size: 30px;
    font-weight: bold;
    color: $title-text-color;
    font-family: serif;
  }

  .text {
    font-size: 14px;
    font-weight: 500;
    color: $sub-title-text-color;
    width: 90%;
    line-height: 1.6;
    word-spacing: 1px;
  }

  .btn {
    background-color: $title-text-color;
    padding: 0.7rem 1.2rem;
    border: none;
    border-radius: 0.3rem;
    color: white;
    font-size: 11px;
    font-weight: 600;
    margin-top: 0.8rem;
    cursor: pointer;
    width: 140px;
  }

  .btn-main {
    transition: 0.3s ease;

    &:hover {
      background-color: #f0edf5;
      color: #58328b;
      transition: 0.3s ease;
    }
  }
}

.over-title {
  font-size: 9px;
  font-weight: 700;
  text-transform: uppercase;
  color: $sub-title-text-color;
  letter-spacing: 1px;
}

.products-carousel {
  display: flex;
  justify-content: space-between;
  width: 68%;
  text-align: center;
  position: relative;
}

.product-title {
  font-size: 18px;
  font-weight: 700;
  color: #58328b;
}

.product-prices {
  font-size: 14px;
  color: #5532a9;
}

.product-text {
  width: 220px;
}

.card {
  transition: transform;
  position: relative;
  cursor: pointer;

  .img-container {
    position: relative;
  }

  .product-layer {
    height: 100%;
    width: 90%;
    background-color: rgba(0, 0, 0, 0.3);
    position: absolute;
    top: -3px;
    left: 11px;
  }
}

.chevron {
  position: absolute;
  top: 120px;
  background-color: #a691b2;
  opacity: 0.7;
  height: 70px;
  width: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 5;
  color: #f8f5f4;
}

.left-chevron {
  left: 10px;
}

.right-chevron {
  right: -30px;
}

.hover-text {
  position: absolute;
  z-index: 2;
  left: 10%;
  right: 30%;
  top: 30%;
  bottom: 30%;
  color: white;
  display: flex;
  text-transform: uppercase;
  width: 90%;

  span {
    font-family: serif;
    font-size: 12px;
    font-weight: 500;
  }
}
</style>