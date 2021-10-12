<template>
  <main>
    <Hero />
    <Mission />
    <Courses />
    <FAQ />
    <Events />
    <Feedback />
  </main>
</template>

<script>
import Hero from "./Hero.vue";
import Mission from "./Mission.vue";
import Courses from "./Courses.vue";
import FAQ from "./FAQ.vue";
import Events from "./Events.vue";
import Feedback from "./Feedback.vue";

export default {
  name: "Main",

  components: {
    Hero,
    Mission,
    Courses,
    FAQ,
    Events,
    Feedback,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
</style>
