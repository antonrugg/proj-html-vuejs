<template>
  <section>
    <!-- //big panel section with text -->
    <div class="text-container">
      <p class="over-title">try our seasonal products</p>
      <p class="title">Order for pick-up or delivery to your home</p>

      <button class="btn btn-header">Shop Now</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "TrySeasonalSection",
};
</script>

<style lang="scss" scoped>
@import "@/styles/generals.scss";

section {
  background-image: url("@/assets/images/call-to-action-bg.jpg");
  background-position: top;
  background-repeat: no-repeat;
  background-size: 100vw;
  background-size: 100vh;
  background-size: cover;
  width: 99vw;
  height: 50vh;
  padding: 2rem 0rem 2rem 2rem;

  .text-container {
    display: flex;
    flex-direction: column;
    width: 60%;
    padding: 2rem 0rem 10rem 17rem;

    .over-title {
      color: #c5bebe;
      font-size: 9px;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .title {
      font-size: 42px;
      font-weight: 700;
      font-family: serif;
      color: white;
      padding: 1rem 0rem 4rem 0rem;
    }

    .btn {
      background-color: white;
      padding: 1rem 1.4rem;
      border: none;
      border-radius: 0.3rem;
      color: #55328b;
      font-size: 14px;
      font-weight: 500;
      margin-top: 0.8rem;
      cursor: pointer;
      width: 150px;
    }

    .btn-header {
      transition: 0.3s ease;

      &:hover {
        background-color: $title-text-color;
        color: white;
        transition: 0.3s ease;
      }
    }
  }
}
</style>