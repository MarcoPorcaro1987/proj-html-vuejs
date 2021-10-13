<template>
  <section class="newsletter">
    <div class="circle-cont">
      <div class="circle"></div>
    </div>
    <div class="email-input-cont">
      <h2>Subscribe <span class="special-color">Newsletters</span></h2>
      <p class="p-text">
        Enter your email address to register to our newsletter subscription
        <br />
        delivered on a regula basis!
      </p>
      <div class="email-submit-cont">
        <input type="email" name="email" placeholder="Enter your email" />
        <div class="btn-common">Subscribe</div>
      </div>
    </div>
    <div class="special-circle-cont">
      <img
        class="special-circle"
        src="../assets/img/maxcoach-shape-02.png"
        alt=""
      />
      <img class="shape-bg" src="../assets/img/maxcoach-shape-09.png" alt="" />
    </div>
  </section>
</template>

<script>
export default {
  name: "Newsletter",
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
.newsletter {
  margin: 0 auto;
  width: 80%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 3rem 0;
  .circle {
    height: 2.5rem;
    width: 2.5rem;
    border: 5px solid #8fd6ca;
    border-radius: 50%;
  }
  .email-input-cont {
    text-align: center;
    .p-text {
      margin: 1.875rem 0;
    }
    input {
      background-color: $bgColor;
      padding: 0.9375rem 3rem;
      border: none;
      border-top-left-radius: 0.3125rem;
      border-bottom-left-radius: 0.3125rem;
      &:focus-visible {
        outline: none;
      }
    }
    .btn-common {
      border-top-left-radius: 0;
      border-bottom-left-radius: 0;
    }
  }
  .special-circle-cont {
    position: relative;
    .shape-bg {
      height: 9.375rem;
      position: absolute;
      left: 0;
    }
  }
}
</style>
