<template>
  <section class="faq">
    <img
      class="transparent-square"
      src="../assets/img/maxcoach-shape-07-150x150.png"
      alt="Bg transparent square"
    />
    <img
      class="transparent-map"
      src="../assets/img/background-map-dots-top-right-transparent.png"
      alt="Bg transparent map"
    />
    <div class="faq-cont">
      <div class="video-faq">
        <img
          class="video-img-bg"
          src="../assets/img/home-business-video-poster-670x450.jpg"
          alt="video img bg"
        />
        <img
          class="youtube-play-img"
          src="../assets/img/icon-youtube-play.png"
          alt="youtube play img"
        />
      </div>
      <div class="question-faq">
        <h2>
          To Thrive In Business <br />
          Today, You'll Need a <br />
          Good Plan
        </h2>
        <div class="questions" v-for="(question, index) in faq" :key="index">
          <i class="fas fa-chevron-circle-down"></i>
          <h4>{{ question.question }}</h4>
          <p>{{ question.answer }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "FAQ",
  data() {
    return {
      faq: [
        {
          question: "How can we help?",
          answer:
            "How many courses you've been on, using however many techniques and methods. Unless you've come to realize the value of mindset, then you've yet to undestand how success comes. With everyone else's mindset involved impacting too. Hence why business coaching is so crucial for success.",
        },
        {
          question: "Why would I need a business COACH?",
          answer: "",
        },
        {
          question: "What is one-on-one coaching?",
          answer: "",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
.faq {
  background-color: #323043;
  position: relative;
  padding: 3.125rem 15rem;
  height: 36.625rem;
  .transparent-map {
    position: absolute;
    top: 0;
    right: 0;
  }
  .transparent-square {
    position: absolute;
    left: 6.25rem;
    bottom: 0;
  }
  .faq-cont {
    margin: 0;
    display: flex;
    height: 100%;
    align-items: center;
    width: 90%;
    gap: 1.875rem;
    .video-faq {
      position: relative;
      .video-img-bg {
        height: 18.75rem;
        object-position: center;
      }
      .youtube-play-img {
        position: absolute;
        height: 3.125rem;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
      }
    }
    .question-faq {
      h2 {
        color: white;
        font-size: 1.875rem;
      }
      .questions {
        display: flex;
        flex-wrap: wrap;
        color: white;
        border-bottom: 0.0625rem solid $secondaryColor;
        padding: 0.9375rem 0;
        align-items: center;
        .fa-chevron-circle-down {
          margin-right: 0.625rem;
        }
        h4 {
          margin: 0.625rem 0;
          color: white;
        }
        p {
          margin-left: 1.625rem;
        }
      }
    }
  }
}
</style>
