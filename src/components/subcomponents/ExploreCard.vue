<template>
  <div class="card h-100">
    <img class="img-fluid" :src="getImg(data.image)" :alt="data.image" />
    <div class="description p-2">
      <h5>{{ data.title }}</h5>
      <p class="m-0">{{ data.description }}</p>
    </div>
    <div
      class="
        box
        d-flex
        justify-content-center
        align-items-center
        border-top
        h-100
      "
    >
      <p class="click m-0">Discover now</p>
      <i class="fas fa-long-arrow-alt-right p-2"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "ExploreCard",
  props: ["data"],
  methods: {
    getImg(image) {
      return require(`@/assets/images/home-business-service-slide-${image}-480x298.jpg`);
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_variables.scss";

.card {
  .box {
    color: $color-jungle-green;
    cursor: pointer;
    &:hover {
      background-color: $color-jungle-green;
      color: $color-white;
    }
  }
}
</style>