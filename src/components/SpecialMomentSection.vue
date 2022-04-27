<template>
  <section>
      <div class="wrapper-display"
           @mouseover="isHover = true"
           @mouseleave="isHover = false">
          <img src="@/assets/images/corporate-bg.jpg" alt="events meetings" v-show="!isHover">
          <img src="@/assets/images/corporate-hover-bg.jpg" alt="events meetings bakery" v-show="isHover">
          <img src="" alt="" v-show="isHover">


          <div class="hover-text" v-show="isHover">
            <p class="over-title">International Bakery</p>
            <h3 class="title">Corporate Events</h3>
            <button class="btn btn-events">Explore more</button>
          </div>
      </div>    
         
      

      <div class="wrapper-display"
           @mouseover="isHover = true"
           @mouseleave="isHover = false">
          <img src="@/assets/images/wedding-bg.jpg" alt="events weddings" v-show="!isHover">
          <img src="@/assets/images/wedding-hover-bg.jpg" alt="cake for weddings" v-show="isHover">


          <div class="hover-text" v-show="isHover">
            <p class="over-title">private dining hall</p>
            <h3 class="title">Weddings & Parties</h3>
            <button class="btn btn-events">Explore more</button>
          </div>
      </div>
      
     
  </section>
</template>

<script>
export default {
    name: 'SpecialMomentSection',
    data(){
      return{
          isHover: false,
      }
  },
}
</script>

<style lang="scss" scoped>
@import "@/styles/generals.scss";

    section{
        display: flex;
        justify-content: space-around;

        img{
            width: 90%;
            cursor: pointer;
        }
    }

    .wrapper-display{
        position: relative;
    }

    .hover-text{
        position: absolute;
        top: 40%;
        right: 40%;
        text-align: center;
        
        .over-title{
            font-size: 12px;
            letter-spacing: 1px;
            color: whitesmoke;
            text-transform: uppercase;
        }

        .title{
            font-size: 22px;
            color: whitesmoke;
            padding: 1.5rem 0rem;
        }

        .btn {
    background-color: $title-text-color;
    padding: 0.7rem 1.4rem;
    border: none;
    border-radius: 0.3rem;
    color: white;
    font-size: 11px;
    font-weight: 600;
    margin-top: 0.8rem;
    cursor: pointer;
    width: 130px;
  }

  .btn-events {
    transition: 0.3s ease;

    &:hover {
      background-color: #f0edf5;
      color: #58328b;
      transition: 0.3s ease;
    }
  }

       
    }


</style>