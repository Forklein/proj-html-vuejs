<template>
  <div class="card p-3">
    <div class="text text-start">
      <h5>{{ data.title }}</h5>
      <p class="my-5">{{ data.description }}</p>
    </div>
    <div class="info d-flex justify-content-start align-items-center">
      <div class="box-img align-self-end">
        <figure class="m-0">
          <img
            :src="getImg(data.image)"
            class="rounded-circle"
            alt="image"
            style="width: 75px"
          />
        </figure>
      </div>
      <div class="author align-self-end text-start">
        <p class="ms-2">{{ data.name }}</p>
        <figcaption class="ms-2">{{ data.job }}</figcaption>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FeedbackCard",
  props: ["data"],
  methods: {
    getImg(image) {
      return require(`@/assets/images/testimonial-avata-${image}.jpg`);
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_variables.scss";
.card {
  min-height: 317px;
  .text {
    p {
      color: $color-boulder;
    }
  }
  h5 {
    color: $color-tuna;
  }
  .author {
    p {
      color: $color-tuna;
    }
  }
}
</style>