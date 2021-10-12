<template>
  <main>
    <Hero />
    <Mission />
    <Courses />
    <FAQ />
  </main>
</template>

<script>
import Hero from "./Hero.vue";
import Mission from "./Mission.vue";
import Courses from "./Courses.vue";
import FAQ from "./FAQ.vue";

export default {
  name: "Main",

  components: {
    Hero,
    Mission,
    Courses,
    FAQ,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
</style>
