<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-6 p-5">
          <p class="fw-bold text-white">Address</p>
          <p class="text-secondary">{{ address.place }}</p>
          <p class="text-secondary">{{ address.hour }}</p>
          <p class="text-secondary">{{ address.email }}</p>
          <div class="row">
            <div class="col d-flex">
              <i class="fab fa-facebook-square fa-2x pe-2 text-secondary"></i>
              <i class="fab fa-twitter fa-2x px-2 text-secondary"></i>
              <i class="fab fa-instagram fa-2x px-2 text-secondary"></i>
              <i class="fab fa-linkedin fa-2x px-2 text-secondary"></i>
            </div>
          </div>
        </div>
        <div class="col-6 p-5">
          <div class="row">
            <div class="col">
              <p class="fw-bold text-white">Explore</p>
              <p v-for="text in explore" class="text-secondary" :key="text">
                {{ text }}
              </p>
            </div>
            <div class="col">
              <p class="fw-bold text-white">Information</p>
              <p v-for="text in information" class="text-secondary" :key="text">
                {{ text }}
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="row text-center text-secondary mt-3">
        <div class="col">
          <p class="fw-bold">© 2020 Maxcoach.All Rights Reserved</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      address: {
        place: "382 NE 191st St # 87394 Miami, FL 33179-3899",
        hour: "+1(305)547-9909(9am - 5pm EST,Monday - Friday)",
        email: "support@maxcoach.com",
      },
      explore: [
        "Start here",
        "Blog",
        "About us",
        "Success story",
        "Courses",
        "Contact us",
      ],
      information: [
        "Membership",
        "Purchase guide",
        "Privacy policy",
        "Terms of service",
      ],
    };
  },
};
</script>

<style scoped lang="scss">
footer {
  background-color: #171621;
}
</style>