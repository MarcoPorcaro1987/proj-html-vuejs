<template>
  <section class="feedback">
    <p class="special-color">People are Prising Maxcoach</p>
    <h2>What make they love us?</h2>
    <div
      class="feedback-cont"
      v-for="(feedback, index) in feedbacks"
      :key="index"
    >
      <h4 class="feedback-title">{{ feedback.title }}</h4>
      <p class="p-text">{{ feedback.comment }}</p>
      <div class="feedback-author">
        <img
          class="author-pic"
          :src="require('../assets/img/' + feedback.pic)"
          :alt="feedback.name"
        />
        <div class="author">
          <p class="author-name">{{ feedback.name }}</p>
          <p class="author-work">{{ feedback.work }}</p>
        </div>
      </div>
    </div>
    <div class="circles-cont">
      <i class="fas fa-circle"></i>
      <i class="fas fa-circle"></i>
      <i class="fas fa-circle"></i>
    </div>
  </section>
</template>

<script>
export default {
  name: "Feedback",
  data() {
    return {
      feedbacks: [
        {
          title: "It's a choice of quality for people with special needs",
          comment:
            "I'm a very strict person so I require everything to be organized and neat. Then, I'll be able to make things right and shine. MaxCoach guys just got me.",
          name: "FLORENCE THEMES",
          pic: "testimonial-avata-03.jpg",
          work: "/ Multimedia Admin",
        },
        {
          title: "High level of efficiency and scientific teaching methods",
          comment:
            "I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.",
          name: "MINA HOLLACE",
          pic: "testimonial-avata-02.jpg",
          work: "/ Freelancer",
        },
        {
          title:
            "Professional team of specialists and passionate mentors at reach",
          comment:
            "I need to get a certification for English proficiency and MaxCoach is my best Choice. Their tutors are smart and professional when dealing with the students.",
          name: "MADLEY PONDOR",
          pic: "testimonial-avata-04.jpg",
          work: "/ IT Specialist",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
.feedback {
  background-color: $bgColor;
  text-align: center;
  padding: 4.375rem;
  display: flex;
  flex-wrap: wrap;
  gap: 2.5rem;
  p,
  h2 {
    width: 100%;
  }
  .feedback-cont {
    padding: 1.875rem;
    margin-top: 2rem;
    background-color: white;
    width: calc(100% / 3 - 2.5rem);
    text-align: left;
    .feedback-title {
      color: $mainColor;
      font-weight: bold;
      margin-bottom: 1.25rem;
    }
    .p-text {
      margin-bottom: 1.875rem;
    }
    .feedback-author {
      display: flex;
      gap: 1.25rem;
      align-items: center;
      img {
        height: 3.125rem;
        border-radius: 50%;
      }
      .author {
        .author-name {
          color: $mainColor;
          margin-bottom: 0.3125rem;
          font-weight: bold;
          font-size: 0.875rem;
        }
        .author-work {
          color: #9c9c9c;
          font-size: 0.75rem;
        }
      }
    }
  }
  .circles-cont {
    margin: 0 auto;
    .fa-circle {
      color: $mainColor;
      margin: 0.625rem;
      font-size: 0.625rem;
    }
  }
}
</style>
