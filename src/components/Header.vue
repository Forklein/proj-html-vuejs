<template>
  <header>
    <div class="container-fluid">
      <div class="row py-3">
        <div class="col-3 d-flex justify-content-center align-items-center">
          <img
            src="../assets/images/dark-logo.png"
            alt="logo"
            style="width: 150px"
          />
        </div>
        <div class="col-6">
          <nav>
            <ul
              class="
                m-0
                list-unstyled
                d-flex
                justify-content-center
                align-items-center
              "
            >
              <li class="px-3" v-for="(nav, index) in navbar" :key="index">
                {{ nav }} <i class="fas fa-angle-down"></i>
              </li>
            </ul>
          </nav>
        </div>
        <div class="col-3 d-flex">
          <div
            class="
              col
              language
              d-flex
              justify-content-center
              align-items-center
              border-end
            "
          >
            <img src="../assets/images/en.png" alt="flag" />
            <p class="m-0 px-2">English</p>
            <i class="fas fa-angle-down px-2"></i>
            <i class="far fa-user-circle px-2"></i>
          </div>
          <div
            class="col search d-flex justify-content-between align-items-center"
          >
            <p class="m-0 px-2">Search...</p>
            <i class="fas fa-search px-2"></i>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      navbar: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_variables.scss";
header {
  nav {
    ul {
      li {
        color: $color-tuna;
        font-size: 21px;
        cursor: pointer;
      }
    }
  }
  i {
    font-size: 12px;
  }
  .language {
    cursor: pointer;
  }
}
</style>