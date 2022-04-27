<template>
  <section class="shopping">
    <div class="text-shopping">
      <p class="over-title">{{ textSections[2].overTitle }}</p>
      <p class="title-main">{{ textSections[2].title }}</p>
      <p class="text">{{ textSections[2].text }}</p>
      <button class="btn btn-main">{{ textSections[2].buttonText }}</button>
    </div>

    <div class="products-carousel">
        <a href="#nowhere"><div class="chevron right-chevron">
            <font-awesome-icon icon="fa-solid fa-chevron-right" /></div></a>
        <a href="#nowhere"><div class="chevron left-chevron">
            <font-awesome-icon icon="fa-solid fa-chevron-left" /></div></a>    
        <div class="card" v-for="product in products" :key="product.id">
            <img :src="require(`@/assets/images/${product.name}-200x255.jpg`)" :alt="product.name">
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
  data(){
      return{
          products: [
              {
                name: 'choco-chip-cookies',
                title: 'Choco Chip Cookies',
                prices: '$19.00 - $39.00',
                id: 1
              },
              {
                name: 'strawberry-jam-cookies',
                title: 'Strawberry Jam Cookies',
                prices: '$24.00 - $62.00',
                id: 2
              },
              {
                name: 'strawberry-donut',
                title: 'Strawberry Donut',
                prices: '$24.00 - $42.00',
                id: 3
              },
              {
                name: 'perfect-macarons',
                title: 'Perfect Macarons',
                prices: '$18.00 - $52.00',
                id: 4
              },
          ]
      }
  }
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

.products-carousel{
    display: flex;
    justify-content: space-between;
    width: 68%;
    text-align: center;
    position: relative;
    
}

.product-title{
    font-size: 18px;
    font-weight: 700;
    color: #58328b;
}

.product-prices{
    font-size: 14px;
    color: #5532a9;
}

.product-text{
    width: 220px;
}

.card{
    transition: transform;
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



</style>