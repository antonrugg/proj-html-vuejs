<template>
  <main class="wrapper">
    <!-- // aside text section, picking the right one with array index -->
    <section class="shopping">
      <div class="text-shopping">
        <p class="over-title">{{ textSections[1].overTitle }}</p>
        <p class="title-main">{{ textSections[1].title }}</p>
        <p class="text">{{ textSections[1].text }}</p>
        <button class="btn btn-main">{{ textSections[1].buttonText }}</button>
      </div>

      <CarouselComponent :carouselItems="carouselItems" />
    </section>

    <SpecialMomentComponent />
    <SpecialMomentSection :events="events" />
    <ProductsShopComponent :textSections="textSections" />
    <BigPanelSectionOne />
    <DoublePanelSection />
    <BigPanelSectionThree />
    <VisitUsComponent />
    <VisitUsMain />
    <StayInTouch />
    <TrySeasonalSection />
  </main>
</template>

<script>
import CarouselComponent from "./CarouselComponent.vue";
import SpecialMomentComponent from "./SpecialMomentComponent.vue";
import SpecialMomentSection from "./SpecialMomentSection.vue";
import ProductsShopComponent from "./ProductsShopComponent.vue";
import BigPanelSectionOne from "./BigPanelSectionOne.vue";
import DoublePanelSection from "./DoublePanelSection.vue";
import BigPanelSectionThree from "./BigPanelSectionThree.vue";
import VisitUsComponent from "./VisitUsComponent.vue";
import VisitUsMain from "./VisitUsMain.vue";
import StayInTouch from "./StayInTouch.vue";
import TrySeasonalSection from "./TrySeasonalSection.vue";

export default {
  name: "MainComponent",
  components: {
    CarouselComponent,
    SpecialMomentComponent,
    SpecialMomentSection,
    ProductsShopComponent,
    BigPanelSectionOne,
    DoublePanelSection,
    BigPanelSectionThree,
    VisitUsComponent,
    VisitUsMain,
    StayInTouch,
    TrySeasonalSection,
  },
  data() {
    return {};
  },
  props: {
    textSections: Array,
    carouselItems: Array,
    events: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/styles/generals.scss";
main {
  margin: auto 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.text-shopping {
  display: flex;
  flex-direction: column;
  width: 33%;
}

.shopping {
  padding-top: 8rem;
  display: flex;

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
</style>
