<template>
  <div class="d-flex">
    <div class="col-1 me-3">
      <i class="fas fa-database fa-2x"></i>
    </div>
    <div class="col text-start">
      <div class="title">
        <h5>{{ data.title }}</h5>
      </div>
      <div class="description">
        <p>{{ data.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LeadingCard",
  props: ["data"],
};
</script>

<style scoped lang="scss">
</style>