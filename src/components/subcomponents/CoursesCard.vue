<template>
  <div
    class="card"
    :style="{
      backgroundImage:
        'url(' +
        require('@/assets/images/stock-full-hd-' +
          data.image +
          '-443x600.jpg') +
        ')',
    }"
  >
    <div
      class="
        description
        d-flex
        flex-column
        justify-content-end
        text-start
        h-100
        p-2
      "
    >
      <h4>{{ data.price }}</h4>
      <p class="fw-bold">{{ data.description }}</p>
      <div class="info-hover d-none">
        <i class="far fa-clipboard pe-2">&nbsp;20 Lessons</i>
        <i class="far fa-user">&nbsp;50 Students</i>
        <p>
          The purpose of this course is to provide the advanced writing
          techniquest commonly used for inspiring readers and ..
        </p>
      </div>
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
@import "../../assets/scss/_variables.scss";
.card {
  height: 500px;
  .description {
    background: linear-gradient(
      to bottom,
      rgba(0, 0, 0, 0.5) 100%,
      rgba(0, 0, 0, 0.1) 30%
    );
    h4 {
      color: $color-jungle-green;
    }
    p {
      color: $color-white;
    }
    i {
      color: $color-white;
    }
  }
  &:hover {
    .info-hover {
      display: block !important;
    }
  }
  cursor: pointer;
}
</style>