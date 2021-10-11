<template>
  <section class="courses">
    <section class="services">
      <div class="mid-container">
        <p class="special-color">Let's Dream Big Together</p>
        <h2>Explore How can I help you</h2>
        <div class="services-cont">
          <div
            class="service-card"
            v-for="(service, index) in services"
            :key="index"
          >
            <img
              :src="require('../assets/img/' + service.img)"
              alt="Consultative Training Pic"
            />
            <div class="service-text-cont">
              <h3>{{ service.title }}</h3>
              <p class="p-text">{{ service.overview }}</p>
            </div>
            <div class="discover-text">
              <p class="special-color">Discover now</p>
              <i class="fas fa-long-arrow-alt-right"></i>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="courses-cont"></section>
  </section>
</template>

<script>
export default {
  name: "Courses",
  data() {
    return {
      services: [
        {
          img: "home-business-service-slide-01-480x298.jpg",
          title: "Consultative Training",
          overview:
            "With a coach addressing multiple issues that are off balance, affecting you business in various unconsidered ways.",
        },
        {
          img: "home-business-service-slide-02-480x298.jpg",
          title: "Real Deal Coaching",
          overview:
            "Brings an exceptionally powerful opportunity. Being able to accept, to work with that opportunity.",
        },
        {
          img: "home-business-service-slide-03-480x298.jpg",
          title: "Advisor Training Program",
          overview:
            "Getting high quality, entrepeneur mindset driven online business coaching, is what is needed.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";

.services {
  background-color: $secondaryColor;
  text-align: center;
  padding: 2.5rem 0;
  h2 {
    margin-top: 0.9375rem;
    margin-bottom: 2.5rem;
  }
  .services-cont {
    display: flex;
    gap: 1.25rem;
    .service-card {
      width: calc(100% / 3 - 1.25rem);
      display: flex;
      flex-direction: column;
      img {
        width: 100%;
      }
      .service-text-cont {
        background-color: white;
        line-height: 2;
        padding: 0.625rem 1.25rem;
        border-bottom: 0.0625rem solid $secondaryColor;
      }
      .discover-text {
        justify-content: center;
        gap: 0.3125rem;
        align-items: center;
        display: flex;
        padding: 0.625rem;
        background-color: white;
        font-size: 0.75rem;
        .fa-long-arrow-alt-right {
          color: $specialColor;
        }
      }
    }
  }
}
</style>
