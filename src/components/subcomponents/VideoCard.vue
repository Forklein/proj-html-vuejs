<template>
  <div class="question mt-5">
    <div @click="openTab(index)" class="title d-flex align-items-center">
      <i
        :class="
          data.done
            ? 'fas fa-chevron-circle-up active'
            : 'fas fa-chevron-circle-down text-white'
        "
        class="px-2"
      ></i>
      <h4 :class="data.done ? 'active' : 'text-white'">
        {{ data.title }}
      </h4>
    </div>
    <div v-if="data.done" class="question-description text-white p-4">
      <p>
        {{ data.description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "VideoCard",
  props: ["data", "index", "dataVideo"],
  methods: {
    openTab(i) {
      this.dataVideo.map((element, index) => {
        if (i === index) {
          element.done = !element.done;
        }
        return element;
      });
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_variables.scss";

.active {
  color: $color-jungle-green;
}
.title {
  cursor: pointer;
}
</style>