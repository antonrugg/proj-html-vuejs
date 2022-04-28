<template>
  <section>
      <div class="wrapper-display"
           @mouseover="showInfos(index)"
           @mouseleave="currentlyShowing = null"
           v-for="(event, index) in events" :key="event.id"
           >
           
           
          <img :src="require(`@/assets/images/${event.src}-bg.jpg`)" alt="events meetings" v-if="currentlyShowing !== index">
          <img :src="require(`@/assets/images/${event.src}-hover-bg.jpg`)" alt="events meetings bakery" v-if="currentlyShowing === index">
         


          <div class="hover-text" v-if="currentlyShowing === index">
            <p class="over-title">{{ event.overTitle }}</p>
            <h3 class="title">{{ event.title }}</h3>
            <button class="btn btn-events">{{ event.btnText }}</button>
          </div>
      </div>    
         
      

      <!-- <div class="wrapper-display"
           @mouseover="showInfos(index)">
          <img src="@/assets/images/wedding-bg.jpg" alt="events weddings" v-if="currentlyShowing === null">
          <img src="@/assets/images/wedding-hover-bg.jpg" alt="cake for weddings" v-if="currentlyShowing === index">


          <div class="hover-text" v-if="currentlyShowing === index">
            <p class="over-title">private dining hall</p>
            <h3 class="title">Weddings & Parties</h3>
            <button class="btn btn-events">Explore more</button>
          </div>
      </div> -->
      
     
  </section>
</template>

<script>
export default {
    name: 'SpecialMomentSection',
    props: {
      events: Array,
    },
    data(){
      return{
          currentlyShowing: null
      }
  },
  methods: {
    showInfos: function (index){
      return this.currentlyShowing = index;
    }
  }
};
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