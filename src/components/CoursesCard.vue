<template>
  <div
    class="card d-flex justify-content-end p-2"
    :style="{
      backgroundImage:
        'url(' +
        require('@/assets/images/stock-full-hd-' +
          data.image +
          '-443x600.jpg') +
        ')',
    }"
  >
    <div class="description text-start">
      <h4>{{ data.price }}</h4>
      <p class="fw-bold">{{ data.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CoursesCard",
  props: ["data"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_variables.scss";

.card {
  height: 500px;
  .description {
    h4 {
      color: $color-jungle-green;
    }
    p {
      color: $color-white;
    }
  }
}
</style>