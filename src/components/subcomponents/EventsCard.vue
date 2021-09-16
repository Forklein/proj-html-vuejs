<template>
  <div class="card d-flex flex-row justify-content-between p-3">
    <div class="info text-start">
      <p id="location">
        <i class="fas fa-map-marker-alt me-2"></i>{{ data.location }}
      </p>
      <h4>{{ data.description }}</h4>
    </div>
    <div class="date">
      <div>
        <p class="h2">{{ data.date }}</p>
        <p class="fw-bold text-uppercase">{{ data.month }}</p>
      </div>
      <p id="ticket" class="m-0 rounded">Get ticket</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "EventsCard",
  props: ["data"],
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_variables.scss";
.card {
  background-color: $color-porcelain;
  #location {
    color: $color-boulder;
  }
  #ticket {
    background-color: $color-jungle-green;
    color: $color-white;
    padding: 5px 20px;
    cursor: pointer;
  }
}
</style>