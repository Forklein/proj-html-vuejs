<template>
  <div class="container pt-5">
    <div class="row">
      <div class="col-3 left"></div>
      <div class="col-6">
        <h1>Subscribe <span>Newsletter</span></h1>
        <p class="p-3 fw-bolder">
          Enter your email address to register to our newsletter subscription
          delivered on a regular basis!
        </p>
        <div class="input-group my-5">
          <input
            type="text"
            class="form-control"
            placeholder="Enter your email"
            aria-label="Recipient's username"
            aria-describedby="button-addon2"
          />
          <button
            class="btn btn-outline-secondary"
            type="button"
            id="button-addon2"
          >
            Subscribe
          </button>
        </div>
      </div>
      <div class="col-3 right"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Newsletter",
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_variables.scss";
.container {
  .left {
    background-image: url("../../assets/images/circle.png");
    background-repeat: no-repeat;
    background-position: center;
  }
  .right {
    background-image: url("../../assets/images/maxcoach-shape-09.png");
    background-repeat: no-repeat;
    background-position: center;
  }
  span {
    color: $color-jungle-green;
  }
  .btn {
    background-color: $color-jungle-green;
    color: $color-white;
  }
  p {
    color: gray;
  }
}
</style>