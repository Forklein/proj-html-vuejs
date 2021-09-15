<template>
  <div>
    <img :src="getImg(data.image)" :alt="data.image" />
    <h5>{{ data.title }}</h5>
    <p>{{ data.description }}</p>
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
</style>