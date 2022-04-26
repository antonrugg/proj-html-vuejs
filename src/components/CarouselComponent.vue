<template>
    <section>
        <a href="#nowhere"><div class="left-arrow"><font-awesome-icon icon="fa-solid fa-chevron-left" /></div></a>
       <a href="#nowhere"><div class="right-arrow"><font-awesome-icon icon="fa-solid fa-chevron-right" /></div></a>
      <div class="card-carousel">  
        <!-- <img :src="'@/assets/images/' + carouselItem.src" alt=""> -->
        
        <img src="@/assets/images/choco-chip-cookies-400x510.jpg" alt="choco chip cookies"/>
        
        <img src="@/assets/images/strawberry-jam-cookies-400x510.jpg" alt="strawberyy jam cookies"/>
        
        
        
      </div>  
    </section>  
</template>

<script>
export default {
    name: 'CarouselComponent',
    props: {
        carouselItems: Array,
        
    },
    
    methods:{
        
    }


}
</script>

<style lang="scss" scoped>
    @import '@/styles/generals.scss';

    // section{
        

    //     .left-arrow{
    //         position: absolute;
    //         left: 48px;
    //         top: 250px;
    //         background-color: $navbar-text-color;
    //         height: 70px;
    //         width: 35px;
    //         display: flex;
    //         align-items: center;
    //         justify-content: center;
    //     }

    //     .right-arrow{
    //         position: absolute;
    //         right: -410px;
    //         top: 250px;
    //         background-color: $navbar-text-color;
    //         height: 70px;
    //         width: 35px;
    //         display: flex;
    //         align-items: center;
    //         justify-content: center;

    //     }
    // }

    .card-carousel{
        display: flex;
        margin-left: 2rem;
        
        img{
            margin-right: 1rem;
        };
    }  
        
    //     img{
    //         margin-right: 1rem;
    //     }

        
    // }

    .fa-chevron-left{
    color: aliceblue;
    }

    .fa-chevron-right{
    color: aliceblue;
    }

</style>