<template>
  <div id="app">
    <Header :navHeader="navHeader" />
    <Main />
    <Footer />
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
      navFooter: [],
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
