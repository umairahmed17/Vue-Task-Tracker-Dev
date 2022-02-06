<template>
  <button @click="onClick($event)" :style="{ background: color }" class="btn">
    {{ text }}
  </button>
</template>
<script>
export default {
  name: "Button",
  props: {
    text: String,
    color: String,
  },
  methods: {
    onClick() {
      this.$emit("toggle-add-task");
    },
  },
  emits: ["toggle-add-task"],
};
</script>
<style></style>
