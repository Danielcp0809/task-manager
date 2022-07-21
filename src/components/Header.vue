<template>
  <header>
    <h1>{{ title }}</h1>
    <Button text="Add Task" color="blue" />
  </header>
</template>
<script>
import Button from "./Button.vue";

export default {
  name: "Header",
  props: {
    title: {
      type: String,
      default: "Hello world",
    },
  },
  components: {
    Button,
  },
};
</script>
<style scoped>
/* scoped means that everything inside the styles is a local style */
header {
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin-bottom: 20px;
}
</style>