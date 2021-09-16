<template>
  <div class="card">
    <img :src="getImg(data.image)" alt="" />
    {{ data.price }}
  </div>
</template>

<script>
export default {
  name: "CoursesCard",
  props: ["data"],
  methods: {
    getImg(image) {
      return require(`@/assets/images/stock-full-hd-${image}-443x600.jpg`);
    },
  },
};
</script>

<style scoped lang="scss">
</style>