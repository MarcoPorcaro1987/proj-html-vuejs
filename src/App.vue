<template>
  <div id="app">
    <Header :navHeader="navHeader" />
    <Main />
    <Footer :navFooter="navFooter" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import "@fortawesome/fontawesome-free/js/all.js";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      navHeader: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
      navFooter: {
        contact: {
          address: "382 NE 191 st ST # 87394 Miami, FL 33179-3899",
          phoneNumber: "+1(305) 547-9909 (9am-5pm EST, Monday-Friday)",
          email: "info@your-company.com",
        },
        social: [
          {
            name: "fab fa-facebook-square",
            link: "#",
          },
          {
            name: "fab fa-twitter",
            link: "#",
          },
          {
            name: "fab fa-instagram",
            link: "#",
          },
          {
            name: "fab fa-linkedin",
            link: "#",
          },
        ],
        explore: [
          {
            content: "Start here",
            link: "#",
          },
          {
            content: "Success story",
            link: "#",
          },
          {
            content: "Blog",
            link: "#",
          },
          {
            content: "Courses",
            link: "#",
          },
          {
            content: "About us",
            link: "#",
          },
          {
            content: "Contact us",
            link: "#",
          },
        ],
        information: [
          {
            content: "Membership",
            link: "#",
          },
          {
            content: "Purchase guide",
            link: "#",
          },
          {
            content: "Privacy policy",
            link: "#",
          },
          {
            content: "Terms of service",
            link: "#",
          },
        ],
      },
    };
  },
};
</script>

<style lang="scss">
// Common
@import "./assets/style/common.scss";
// Variables
@import "./assets/style/variables.scss";
// Google Font (Roboto)
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap");
</style>
