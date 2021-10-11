<template>
  <main>
    <Hero />
    <Mission />
  </main>
</template>

<script>
import Hero from "./Hero.vue";
import Mission from "./Mission.vue";

export default {
  name: "Main",

  components: {
    Hero,
    Mission,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
</style>
