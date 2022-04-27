<template>
  <section>
      <div class="left-panel">
          <div class="product-layer"></div>
        <div class="title-container">
          <h3 class="title">We Start Baking</h3>
          <p class="panel-order">02</p>
        </div>

        <div class="description-container">
        <div class="text-container">
          <p class="over-text">sweet & delicious</p>
          <p class="text">Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec lorem erat, finibus in velit placerat.</p>
        </div>
      </div>
      </div>
      <div class="right-panel">
          <p class="over-text">dont just take our word for it</p>
          <h3 class="title">“Finalli found an alternative to the mass produced products. Something that incorporates real organiz ingredients, nutrient dense wellness while promoting sustainability and activity.”</h3>
          <p class="signature">Rachel Cooper, Founder</p>
      </div>
  </section>
</template>

<script>
export default {
    name: 'DoublePanelSection',

}
</script>

<style lang="scss" scoped>
@import "@/styles/generals.scss";

section{
    display: flex;
    justify-content: space-between;
    padding-top: 2rem;
    margin: auto 2.5%;

     .over-text{
        color: #c7ccd2;
        text-transform: uppercase;
        word-spacing: 1px;
        font-size: 11px;
                        }
    

    .left-panel{
        background-image: url('@/assets/images/bakery-process-2.jpg');
        width: 49%;
        background-size: cover;
        background-position: top right;
        padding: 5rem 5rem 3rem 5rem;
        position: relative;
        z-index: 0;
        
        

        .title-container{
            display: flex;
            color: white;
            justify-content: space-between;
            padding-bottom: 10rem;
            z-index: 3;
            
            

            .title{
                font-size: 42px;
                font-weight: 700;
                font-family: serif;
                width: 90%;
                padding-top: 0.8rem;
            }

            .panel-order{
                font-size: 72px;
                font-weight: lighter;
            }



        }

         .description-container{
            display: flex;
            justify-content: flex-start;
            align-items: flex-start;
            z-index: 3;

             .text-container{
                    display: flex;
                    flex-direction: column;
                    align-items: flex-start;
                    width: 64%;
                    text-align: left;
                    
    
                    p{
                        padding-bottom: 0.7rem;
    
                        
                    }
                   
    
                    .text{
                        color: white;
                        line-height: 1.6;
                        word-spacing: 1px;
                    }    
             }
         }
    
        .product-layer{
        height: 100%;
        width: 100%;
        background-color: rgba(0, 0, 0, 0.4);
        position: absolute;
        top: 0;
        left: 0;
        z-index: -1;
    }
    }

    .right-panel{
        background-color: #f2eef5;
        width: 49%;
        padding-top: 5rem;
        padding-left: 3rem;
        padding-right: 1.8rem;
        text-align: left;

        .over-text{
            color: #74727d;
            font-size: 10px;
        }

        .title{
            font-size: 40px;
            font-weight: bold;
            color: #55328b;
            font-family: serif;
            padding: 1.8rem 0rem;
            
        }

        .signature{
            color: #74727d;
            word-spacing: 1px;
            font-size: 12px;
        }
    }
    

    
       
}
</style>