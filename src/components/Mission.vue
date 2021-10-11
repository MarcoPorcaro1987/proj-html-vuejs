<template>
  <section class="mid-container mission-cont">
    <p class="special-color">Let's Dream Big Together</p>
    <h2>
      We are pioneers of the digital approach, using leading-edge <br />
      technology to simplify procedures and apply executive <br />
      coaching in the new age of digitalization.
    </h2>
    <div class="features-cont">
      <div class="feature" v-for="(feature, index) in features" :key="index">
        <h3>{{ feature.title }}</h3>
        <p class="p-text">{{ feature.overview }}</p>
      </div>
    </div>
    <div class="btn-cont">
      <div class="btn-common bg-white">Learn more</div>
      <div class="btn-common">Get started today</div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Mission",
  data() {
    return {
      features: [
        {
          title: "One to One",
          overview:
            "Getting the necessary clarity about the current state to help you improve your game.",
        },
        {
          title: "Anywhere",
          overview:
            "Access to valuable and portable program which allow you to setup and live anywhere you want.",
        },
        {
          title: "On Time",
          overview:
            "Punctually is our top priority because it's an essential criteria to assess a program quality.",
        },
        {
          title: "Online Courses",
          overview:
            "Online business coaching now offers you a very powerful way to empower your business into success.",
        },
        {
          title: "Consulting",
          overview:
            "You will get a clear sens of direction for your business, through assessment and faster results.",
        },
        {
          title: "Self Development",
          overview:
            "Business Coaching often keep you focus and develop you both in a professional and personal way.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";

.mission-cont {
  text-align: center;
  padding: 3.125rem 0;
  h2 {
    margin: 1.875rem 0;
  }
  .features-cont {
    margin: 5rem 0;
    display: flex;
    flex-wrap: wrap;
    text-align: left;
    gap: 2.5rem;
    .feature {
      width: calc(100% / 3 - 2.5rem);
      h3 {
        margin-bottom: 20px;
      }
    }
  }
  .btn-common {
    margin: 0 1.25rem;
  }
  .bg-white {
    background-color: white;
    color: $specialColor;
    border: 1px solid $secondaryColor;
    padding: 0.9375rem 3rem;
  }
}
</style>
