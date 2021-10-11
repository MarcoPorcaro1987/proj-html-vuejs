<template>
  <header>
    <div class="logo-cont">
      <img
        class="logo"
        :src="require('../assets/img/' + image)"
        alt="logo MaxCoach"
      />
    </div>
    <nav>
      <ul class="nav-cont">
        <li v-for="(link, index) in navHeader" :key="index">
          <a href="#">{{ link }} <i class="fas fa-chevron-down"></i></a>
        </li>
      </ul>
    </nav>
    <div class="buttons-cont">
      <div class="lang-cont">
        <img src="../assets/img/en.png" alt="En Flag" />
        <div>ENGLISH</div>
        <i class="fas fa-chevron-down"></i>
      </div>
      <div class="user-icon">
        <i class="far fa-user-circle"></i>
      </div>
      <input type="search" placeholder="Search..." />
      <i class="fas fa-search"></i>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["navHeader"],

  data() {
    return {
      image: "dark-logo.png",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
header {
  display: flex;
  padding: 0 1rem;
  justify-content: space-between;
  align-items: center;
  .logo {
    height: 1.25rem;
    margin-left: 6.25rem;
  }
  .nav-cont,
  .buttons-cont,
  .lang-cont {
    display: flex;
    align-items: center;
    .fa-chevron-down {
      font-size: 0.625rem;
    }
  }
  .nav-cont {
    gap: 1.25rem;
    a {
      color: $mainColor;
    }
  }
  .buttons-cont,
  .lang-cont {
    gap: 0.625rem;
    input {
      padding: 1.875rem 0.625rem;
      border: none;
      border-left: 0.0625rem solid $secondaryColor;
      outline: none;
    }
  }
}
</style>
