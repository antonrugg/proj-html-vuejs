<template>
  <section>
    <!-- big panel section with text inside -->
    <div class="product-layer"></div>
    <div class="title-container">
      <h3 class="title">Tell us what you have in mind</h3>
      <p class="panel-order">01</p>
    </div>

    <div class="description-container">
      <div class="text-container">
        <p class="over-text">manual ingredients selection</p>
        <p class="text">
          Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl
          varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam quis sagittis
          nibh. Morbi consectetur ultricies ante ac congue. Donec lorem erat,
          finibus in velit placerat, rutrum augue.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BigPanelSectionOne",
  data() {
    return {
   
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  display: flex;
  flex-direction: column;
  background-image: url("@/assets/images/bakery-process-1.jpg");
  background-size: cover;
  background-position: top left;
  padding: 5rem 5rem 3rem 5rem;
  width: 95%;
  position: relative;

  .title-container {
    display: flex;
    color: white;
    justify-content: space-between;
    padding-bottom: 10rem;
    z-index: 2;

    .title {
      font-size: 42px;
      font-weight: 700;
      font-family: serif;
      width: 40%;
    }

    .panel-order {
      font-size: 72px;
      font-weight: lighter;
    }
  }

  .description-container {
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    z-index: 2;

    .text-container {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      width: 38%;

      p {
        padding-bottom: 0.7rem;
      }
      .over-text {
        color: #8f8889;
        text-transform: uppercase;
        word-spacing: 1px;
        font-size: 10px;
      }

      .text {
        color: white;
        line-height: 1.6;
        word-spacing: 1px;
      }
    }
  }

  .product-layer {
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.4);
    position: absolute;
    top: 0;
    left: 0;
  }
}
</style>