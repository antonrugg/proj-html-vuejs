<template>
  <footer>
    <div class="footer-left">
      <LogoComponent />
      <FooterNavBarComponent :footerLinks="footerLinks" />
      <div class="copyrights">
        <p>
          © Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights
          Reserved | Powered by WordPress
        </p>
      </div>
    </div>

    <div class="footer-right">
      <p class="title">Subscribe to our Newsletter</p>
      <input type="email" placeholder="Enter email address*" />
      <button class="btn btn-main">Subscribe</button>

      <div class="icon-container">
        <ul>
          <li><font-awesome-icon icon="fa-brands fa-instagram" /></li>
          <li><font-awesome-icon icon="fa-brands fa-twitter" /></li>
          <li><font-awesome-icon icon="fa-brands fa-facebook-f" /></li>
          <li><font-awesome-icon icon="fa-brands fa-pinterest-p" /></li>
        </ul>
      </div>
    </div>

    <div class="scroll-up">
      <a href=""><font-awesome-icon icon="fa-solid fa-chevron-up" /></a>
    </div>
  </footer>
</template>

<script>
import FooterNavBarComponent from "@/components/FooterNavBarComponent.vue";
import LogoComponent from "@/components/LogoComponent.vue";

export default {
  name: "FooterComponent",
  components: {
    FooterNavBarComponent,
    LogoComponent,
  },
  props: {
    footerLinks: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/styles/generals.scss";
footer {
  margin: auto 5%;
  padding: 2rem 0rem 7rem 0rem;
  display: flex;
  justify-content: space-between;
  position: relative;

  .scroll-up{
    background-color: #474747;
    height: 30px;
    width: 30px;
    border-radius: 4px;
    padding: 0.5rem;
    color: white;
    position: absolute;
    bottom: 70px;
    right: 0px;

    a{
      color: white;
    }
  }

  .copyrights {
    font-size: 9px;
    color: #908d97;
    padding-top: 4rem;
  }

  .footer-right {
    .title {
      font-size: 22px;
      font-weight: bold;
      color: #55328b;
      font-family: serif;
      text-align: right;
      padding: 2.5rem 0rem 1.5rem 0rem;
    }

    input {
      padding: 9px 20px;
      margin: 8px 0;
      box-sizing: border-box;
      border: 1px solid #ccc;
      -webkit-transition: 0.5s;
      transition: 0.5s;
      outline: none;
      border-radius: 5px;
      width: 340px;

      &:focus {
        border: 3px solid #555;
      }
    }

    .btn {
      background-color: $title-text-color;
      padding: 0.8rem 1.4rem;
      border: none;
      border-radius: 0.3rem;
      color: white;
      font-size: 11px;
      font-weight: 600;
      margin-top: 0.8rem;
      cursor: pointer;
      width: 120px;
      text-align: center;
      margin-left: 1rem;
    }

    .btn-main {
      transition: 0.3s ease;

      &:hover {
        background-color: #f0edf5;
        color: #58328b;
        transition: 0.3s ease;
      }
    }

    .icon-container {
      padding-top: 5rem;



      ul {
        display: flex;
        justify-content: flex-end;
        li {
          list-style-type: none;
          padding: 0rem 1rem;
          color: #55328b;
        }
      }
    }
  }
}
</style>
