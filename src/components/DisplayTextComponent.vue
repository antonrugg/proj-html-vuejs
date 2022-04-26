<template>
  <section>
      <p class="over-title">{{ textSections.overTitle }}</p>
      <p class="title">{{ textSections.title }}</p>
      <p class="text">{{ textSections.text }}</p>
      <button class="btn"> {{ textSections.buttonText }} </button>
  </section>
</template>

<script>
export default {
    name: 'DisplayTextComponent',
    props: {
      textSections: Object,
    }
}
</script>

<style lang="scss" scoped>
     @import '@/styles/generals.scss';

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
        }
    }

</style>