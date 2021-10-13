<template>
  <footer>
    <div class="mid-container">
      <div class="nav-cont address">
        <h5>Address</h5>
        <p>{{ navFooter.contact.address }}</p>
        <p>{{ navFooter.contact.phoneNumber }}</p>
        <p>{{ navFooter.contact.email }}</p>
        <div class="social">
          <a
            class="social-link"
            v-for="(sn, index) in navFooter.social"
            :key="index"
            :href="sn.link"
          >
            <i :class="sn.name"></i>
          </a>
        </div>
      </div>
      <div class="nav-cont explore">
        <h5>Explore</h5>
        <p v-for="(link, index1) in navFooter.explore" :key="index1">
          <a :href="link.link">{{ link.content }}</a>
        </p>
      </div>
      <div class="nav-cont information">
        <h5>Information</h5>
        <p v-for="(link, index2) in navFooter.information" :key="index2">
          <a :href="link.link">{{ link.content }}</a>
        </p>
      </div>
    </div>
    <div class="footer-bottom-cont">
      <p class="copyrights-text">
        <span>&copy;</span>2020 Maxcoach. All Rights Reserved
      </p>
      <div class="back-to-top-button">
        <a href="#"> <i class="fas fa-long-arrow-alt-up"></i></a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: ["navFooter"],
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
footer {
  padding: 2.5rem 0;
  background-color: #171621;
  a,
  p {
    color: #a0a0a1;
    font-size: 0.75rem;
  }
  h5 {
    color: white;
    margin-bottom: 0.625rem;
  }
  .mid-container {
    display: flex;
    .address {
      width: 50%;
      p {
        width: 100%;
      }
      .social-link {
        margin-right: 1.25rem;
      }
    }
    .nav-cont {
      display: flex;
      flex-wrap: wrap;
      line-height: 2;
      h5 {
        width: 100%;
      }
    }
    .explore {
      width: 30%;
      p {
        width: 50%;
      }
    }
    .information {
      p {
        width: 100%;
      }
    }
  }
  .footer-bottom-cont {
    margin-top: 3.125rem;

    .copyrights-text {
      text-align: center;
    }
    .back-to-top-button {
      text-align: center;
      line-height: 1.875rem;
      margin-left: auto;
      margin-right: 1.25rem;
      height: 1.875rem;
      width: 1.875rem;
      border-radius: 50%;
      background-color: $specialColor;
      .fa-long-arrow-alt-up {
        color: white;
      }
    }
  }
}
</style>
