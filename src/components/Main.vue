<template>
  <main class="text-center">
    <section class="jumbotron">
      <div class="container">
        <div class="row">
          <div class="col-6 d-flex justify-content-center align-items-center">
            <div class="jumbotron-text text-start">
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
              <div class="button w-50 px-3 py-3 rounded text-center">
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
            <div class="icons bg-white d-flex flex-column rounded">
              <i class="fas fa-ruler p-2"></i>
              <i class="far fa-life-ring p-2"></i>
              <i class="far fa-sticky-note p-2"></i>
              <i class="fas fa-shopping-cart p-2"></i>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="leading-edge mt-5">
      <div class="container">
        <div class="row">
          <h4 class="p-3">Let's Dream Big Together</h4>
          <h2 class="p-3 fw-bold">
            We Are pioneers of the digital approach, using leading-edge <br />
            technology to simplify procedures and apply executive <br />
            coaching in the new age of digitalization.
          </h2>
        </div>
        <div class="row mt-5">
          <div v-for="(data, index) in dataLeading" :key="index" class="col-4">
            <LeadingCard :data="data" />
          </div>
        </div>
        <div class="row mt-5">
          <div class="col-6 mx-auto d-flex justify-content-evenly">
            <p class="m-0 p-3 first border rounded">Learn more</p>
            <p class="m-0 p-3 second rounded">Get started today</p>
          </div>
        </div>
      </div>
    </section>
    <section class="explore mt-5">
      <div class="container">
        <div class="row pt-5 mb-5">
          <h4>Let's Dream Big Together</h4>
          <h1 class="p-2 fw-bold">Explore How can I help you</h1>
        </div>
        <div class="row mb-5 pb-5">
          <div v-for="(data, index) in dataExplore" :key="index" class="col-4">
            <ExploreCard :data="data" />
          </div>
          <div class="col-6 mx-auto d-flex justify-content-center mt-5">
            <div
              v-for="(data, index) in dataExplore"
              :key="index"
              class="ball m-2"
            ></div>
          </div>
        </div>
      </div>
    </section>
    <section class="courses">
      <div class="container">
        <div class="row pt-5 mb-5">
          <h4>Let's Dream Big Together</h4>
          <h1 class="p-2 fw-bold">Explore How can I help you</h1>
        </div>
        <div class="row mb-5">
          <div v-for="(data, index) in dataCourses" :key="index" class="col-3">
            <CoursesCard :data="data" />
          </div>
          <div class="col-6 mx-auto mt-5">
            <p>
              Take the control of their life back and start doing things to make
              their dream come true.
              <strong><u>View all courses</u></strong>
              <i class="fas fa-long-arrow-alt-right p-2"></i>
            </p>
          </div>
        </div>
      </div>
    </section>
    <section class="video">
      <div class="container-fluid h-100">
        <div class="row h-100">
          <div class="col-6 left">
            <div class="row align-items-center h-100">
              <div
                class="
                  youtube-box
                  col-9
                  ms-auto
                  d-flex
                  justify-content-center
                  align-items-center
                "
              >
                <div class="icon">
                  <img
                    src="../assets/images/icon-youtube-play.png"
                    alt="youtube"
                  />
                </div>
              </div>
            </div>
          </div>
          <div class="col-6 right"></div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
//# Data
import dataLeading from "@/assets/data/dataLeading.js";
import dataExplore from "@/assets/data/dataExplore.js";
import dataCourses from "@/assets/data/dataCourses.js";

//# Components
import LeadingCard from "@/components/LeadingCard.vue";
import ExploreCard from "@/components/ExploreCard.vue";
import CoursesCard from "@/components/CoursesCard.vue";

export default {
  name: "Main",
  components: {
    LeadingCard,
    ExploreCard,
    CoursesCard,
  },
  data() {
    return {
      dataLeading,
      dataExplore,
      dataCourses,
    };
  },
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
  .leading-edge {
    h4 {
      color: $color-jungle-green;
    }
    p {
      &.first {
        color: $color-jungle-green;
      }
      &.second {
        background-color: $color-jungle-green;
        color: $color-white;
      }
    }
  }
  .explore {
    background-color: $color-porcelain;
    h4 {
      color: $color-jungle-green;
    }
    .ball {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background-color: black;
    }
  }
  .courses {
    h4 {
      color: $color-jungle-green;
    }
  }
  .video {
    height: 800px;
    background-color: $color-tuna;
    .left {
      background-image: url("../assets/images/maxcoach-shape-07.png");
      background-repeat: no-repeat;
      background-position: 20% 90%;
      .youtube-box {
        background-image: url("../assets/images/home-business-video-poster-670x450.jpg");
        background-size: cover;
        height: 450px;
      }
    }
    .right {
      background-image: url("../assets/images/background-map-dots-top-right-transparent.png");
      background-repeat: no-repeat;
    }
  }
}
</style>