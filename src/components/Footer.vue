<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-6"></div>
        <div class="col-6"></div>
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
  height: 500px;
  background-color: #171621;
}
</style>