<script setup>
import TodoItem from './TodoItem.vue';

const tasks = {
  task1: {
    text: "wash up",
    complete: false,
  },
  task3: {
    text: "wash up",
    complete: false,
  },
  task2: {
    text: "wash up",
    complete: false,
  }
};

</script>

<template>
  <div v-for="task in tasks">
    {{ task.text }}
  </div>

  <TodoItem/>

</template>

<style scoped>
</style>
