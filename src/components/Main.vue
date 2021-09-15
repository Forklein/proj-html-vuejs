<template>
  <main>
    <div class="jumbotron">
      <div class="container">
        <div class="row">
          <div class="col-6 d-flex justify-content-center align-items-center">
            <div class="jumbotron-text">
              <h3>New Challenges, New Skills</h3>
              <h1 class="py-3 fw-bold">
                BUILD YOUR OWN <br />
                LIFE COACHING <br />
                BUSINESS
              </h1>
              <h5 class="py-3">
                Whole-Life Business Coaching for committed <br />
                entrepreneurs
              </h5>
              <div class="button w-50 text-center px-3 py-3 rounded">
                <p class="m-0">Get started today</p>
              </div>
            </div>
          </div>
          <div class="col-6 d-flex earth">
            <div class="align-items-stretch">
              <img
                src="../assets/images/home-business-hero-avatar.png"
                alt=""
              />
            </div>
            <div class="icons bg-white d-flex flex-column text-center rounded">
              <i class="fas fa-ruler p-2"></i>
              <i class="far fa-life-ring p-2"></i>
              <i class="far fa-sticky-note p-2"></i>
              <i class="fas fa-shopping-cart p-2"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "Main",
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_variables.scss";

main {
  .jumbotron {
    position: relative;
    background-color: $color-porcelain;
    h3 {
      color: $color-jungle-green;
    }
    h5 {
      color: $color-boulder;
    }
    .button {
      background-color: $color-jungle-green;
      color: $color-white;
    }
    .earth {
      background-image: url("../assets/images/home-business-hero-global-image.png");
    }
    .icons {
      position: absolute;
      top: 20%;
      right: 20px;
    }
  }
}
</style>