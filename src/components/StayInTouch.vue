<template>
  <section>
    <div class="row">
      <div class="img-container">
        <img src="@/assets/images/social-1.jpg" alt="" />
      </div>
      <div class="stay-in-touch-container">
        <div class="sub-section-text">
          <p>made for sharing</p>
        </div>
        <div class="stay-in-touch-title">
          <h3>Let's stay in touch</h3>
        </div>

        <button class="btn btn-main">
          <font-awesome-icon icon="fa-brands fa-instagram" />Follow Us
        </button>
      </div>
      <div class="img-container">
        <img src="@/assets/images/social-2.jpg" alt="" />
      </div>
    </div>

    <div class="row">
      <div class="img-container">
        <img src="@/assets/images/social-3.jpg" alt="" />
      </div>
      <div class="img-container">
        <img src="@/assets/images/social-4.jpg" alt="" />
      </div>
      <div class="img-container">
        <img src="@/assets/images/social-5.jpg" alt="" />
      </div>
      <div class="img-container">
        <img src="@/assets/images/social-6.jpg" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "StayInTouch",
};
</script>

<style lang="scss" scoped>
@import "@/styles/generals.scss";
section {
  margin: auto 5%;
  padding-top: 10rem;

  .row {
    display: flex;
    justify-content: space-between;
    column-gap: 2.1rem;

    .stay-in-touch-container {
      background-color: #f7f0f3;
      width: 100%;
      max-height: 290px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;

      .sub-section-text {
        color: #878691;
        font-size: 9px;
        font-weight: 500;
        text-transform: uppercase;
        letter-spacing: 1px;
      }

      .stay-in-touch-title {
        font-size: 28px;
        font-weight: bold;
        color: $title-text-color;
        font-family: serif;
        text-align: center;
        padding: 1.5rem 0rem 1.5rem 0rem;
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
        width: 120px;
        text-align: center;

        .fa-instagram{
            padding-right: 0.3rem;
        }


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

    img {
      width: 300px;
      max-height: 350px;
      padding-bottom: 1.5rem;
    }
  }
}
</style>


