<template>
  <main>
    <Hero />
    <Mission />
    <Courses />
  </main>
</template>

<script>
import Hero from "./Hero.vue";
import Mission from "./Mission.vue";
import Courses from "./Courses.vue";

export default {
  name: "Main",

  components: {
    Hero,
    Mission,
    Courses,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
</style>
