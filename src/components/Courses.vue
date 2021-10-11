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
              alt="service.title"
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
        <div class="circles-cont">
          <i class="fas fa-circle"></i>
          <i class="fas fa-circle"></i>
          <i class="fas fa-circle"></i>
        </div>
      </div>
    </section>
    <section class="plans-cont">
      <p class="special-color">Let's Dream Big Together</p>
      <h2>Explore How can I help you</h2>
      <div class="plan-cont">
        <div class="plan-card" v-for="(plan, index) in plans" :key="index">
          <img :src="require('../assets/img/' + plan.img)" alt="plan.title" />
          <div class="plan-text">
            <p class="special-color">{{ plan.price }}</p>
            <p class="plan-title">{{ plan.title }}</p>
          </div>
        </div>
      </div>
      <div class="plan-link">
        <p class="special-color">
          Take the control of their life back and start doing things to make
          their <br />
          dream come true.
          <span class="text-link"
            >View all courses <i class="fas fa-long-arrow-alt-right"></i
          ></span>
        </p>
      </div>
    </section>
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
      plans: [
        {
          img: "course-02-443x600.jpg",
          price: "$40.oo",
          title: "Learning to Write as a Professional Author",
        },
        {
          img: "stock-full-hd-03-443x600.jpg",
          price: "Free",
          title: "Customer-centric Info-Tech Strategies",
        },
        {
          img: "stock-full-hd-04-443x600.jpg",
          price: "$19.oo",
          title: "Open Programming Courses for Everyone: Python",
        },
        {
          img: "stock-full-hd-06-443x600.jpg",
          price: "$26.oo",
          title: "Academic Listening and Note-taking",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";

//Common
h2 {
  margin-top: 0.9375rem;
  margin-bottom: 2.5rem;
}

//Services Section
.services {
  background-color: $secondaryColor;
  text-align: center;
  padding: 2.5rem 0;
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
  .circles-cont {
    margin-top: 1.875rem;
    .fa-circle {
      margin: 0 0.3125rem;
      font-size: 0.625rem;
    }
  }
}

//Plans Section
.plans-cont {
  margin: 0 auto;
  padding: 1.875rem 0;
  width: 80%;
  text-align: center;
  .plan-cont {
    display: flex;
    gap: 1.25rem;
    .plan-card {
      width: calc(100% / 4 - 1.25rem);
      position: relative;
      img {
        width: 100%;
      }
      .plan-text {
        background: linear-gradient(to top, black, transparent);
        position: absolute;
        text-align: left;
        bottom: 0px;
        left: 0px;
        padding: 0.625rem;
        padding-right: 2.5rem;
      }
      .plan-title {
        color: white;
      }
    }
  }
  .plan-link {
    margin-top: 1.875rem;
    span {
      color: $titleColor;
      border-bottom: 0.0625rem solid $secondaryColor;
      font-weight: bold;
    }
  }
}
</style>
