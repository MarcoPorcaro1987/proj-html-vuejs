<template>
  <section class="hero">
    <div class="btn-cont">
      <i class="fas fa-ruler-combined"></i>
      <i class="far fa-life-ring"></i>
      <i class="fas fa-book"></i>
      <i class="fas fa-shopping-cart"></i>
    </div>
    <div class="mid-container hero-cont">
      <div class="hero-text">
        <p class="special-color">New Challanges, New Skills</p>
        <h1>
          BUILD YOUR OWN <br />
          LIFE COACHING <br />
          BUSINESS
        </h1>
        <div class="p-text">
          Whole-Life Business Coaching for committed <br />
          entrepreneurs
        </div>
        <div class="btn-common">Get started today</div>
      </div>
      <div class="hero-img">
        <img
          class="hero-global-image"
          src="../assets/img/home-business-hero-global-image.png"
          alt="Hero Global Image"
        />
        <img
          class="hero-avatar-image"
          src="../assets/img/home-business-hero-avatar.png"
          alt="Hero Avatar Image"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";

.hero {
  background-color: $secondaryColor;
  position: relative;
  .btn-cont {
    padding: 0.625rem;
    background-color: white;
    position: absolute;
    right: 0;
    top: 4.375rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.625rem;
    font-size: 0.625rem;
  }
  .hero-cont {
    display: flex;
    height: 31.25rem;
    .hero-text {
      width: 40%;
      align-self: center;
      > * {
        margin-bottom: 1.25rem;
      }
      h1 {
        font-weight: 900;
      }
    }
    .hero-img {
      position: relative;
      width: 60%;
      .hero-global-image,
      .hero-avatar-image {
        position: absolute;
        height: 100%;
      }
      .hero-avatar-image {
        padding-top: 3.125rem;
      }
      .hero-global-image {
        padding-bottom: 3.125rem;
      }
    }
  }
}
</style>
