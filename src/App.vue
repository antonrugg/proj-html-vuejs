<template>
  <div id="app">
    <HeaderComponent :headerLinks="headerLinks" :textSections="textSections" />
    <MainComponent
      :textSections="textSections"
      :carouselItems="carouselItems"
      :events="events"
    />
    <FooterComponent :footerLinks="footerLinks" />
  </div>
</template>

<script>
import HeaderComponent from "@/components/HeaderComponent.vue";
import MainComponent from "@/components/MainComponent.vue";
import FooterComponent from "@/components/FooterComponent.vue";
//imported components

import headerLinks from "@/assets/data/header-nav";
import footerLinks from "@/assets/data/footer-nav";
import textSections from "@/assets/data/display-text";
import carouselItems from "@/assets/data/carousel";
import events from "@/assets/data/events";
//imported json datas

export default {
  name: "App",
  data() {
    return {
      headerLinks,
      footerLinks,
      textSections,
      carouselItems,
      events,
    };
  },
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent,
  },
};
</script>

<style lang="scss">
@import "@/styles/generals.scss";
</style>
