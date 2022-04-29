<template>
  <section>
    <!-- single card ny -->
    <div class="city-card bg-ny">
      <img
        src="@/assets/images/new-york-bk-800x530.jpg"
        alt="london location"
      />
      <div class="bottom-section">
        <p class="title">New York</p>

        <div class="bottom-sub-section">
          <div class="sub-section-text">
            <p>call us</p>
            <p>1.800.458.556</p>
          </div>

          <div class="sub-section-text">
            <p>open all week</p>
            <p>9:00 AM - 6:00 PM</p>
          </div>

          <button class="btn btn-header">View Map</button>
        </div>
      </div>
    </div>

<!-- single card london -->
    <div class="city-card bg-lnd">
      <img src="@/assets/images/london-bk-800x530.jpg" alt="london location" />
      <div class="bottom-section">
        <p class="title">London</p>

        <div class="bottom-sub-section">
          <div class="sub-section-text">
            <p>call us</p>
            <p>1.800.458.556</p>
          </div>

          <div class="sub-section-text">
            <p>open all week</p>
            <p>9:00 AM - 6:00 PM</p>
          </div>

          <button class="btn btn-header">View Map</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "VisitUsMain",
};
</script>

<style lang="scss" scoped>
@import "@/styles/generals.scss";
section {
  display: flex;
  margin: auto 2.5%;

  .bg-ny {
    background-color: #f1f9fb;
  }

  .bg-lnd {
    background-color: #faf3e3;
  }

  .city-card {
    display: flex;
    flex-direction: column;
    width: 50%;
    padding: 0rem 0rem 3rem 0rem;

    img {
      width: 100%;
    }

    .title {
      font-size: 28px;
      font-weight: bold;
      color: $title-text-color;
      font-family: serif;
      text-align: center;
      padding: 2.5rem 0rem 1.5rem 0rem;
    }

    .bottom-section {
      display: flex;
      flex-direction: column;
    }

    .bottom-sub-section {
      display: flex;
      justify-content: space-evenly;

      .sub-section-text {
        color: #878691;
        font-size: 10px;
        font-weight: 600;
        text-transform: uppercase;

        p {
          padding: 0.5rem 0rem;
          text-align: center;
        }
      }

      .btn {
        background-color: white;
        padding: 0.4rem 1.4rem;
        border: none;
        border-radius: 0.3rem;
        color: $navbar-text-color;
        font-size: 11px;
        font-weight: 600;
        cursor: pointer;
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
}
</style>


