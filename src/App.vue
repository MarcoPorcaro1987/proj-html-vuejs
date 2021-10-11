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
@import "./assets/style/common.scss";
@import "./assets/style/variables.scss";
</style>
