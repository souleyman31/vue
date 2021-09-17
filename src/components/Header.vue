<template>
  <header>
    <h1>{{ title }}</h1>

    <Button
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
    <!-- <Button text="Update Task " color="yellow" />
    <Button text="Delete Task " color="red" /> -->
  </header>
</template>

<script>
import Button from "./Button.vue";
export default {
  name: "Header",
  props: {
    title: String,
    showAddTask: Boolean
  },
  components: { Button }
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
  /* color: blue; */
}
</style>
