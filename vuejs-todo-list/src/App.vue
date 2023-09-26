<script setup>
  import TodoItem from './components/TodoItem.vue';
  import TodoInput from './components/TodoInput.vue';
  import { ref } from 'vue';

  let tasks = ref([]) 

  const updateTasks = (newTasks) => {
    tasks.value = newTasks
  }
</script>

<template>
  <main>
    <div class="list">
      <h1>To-Do List</h1>
      <TodoInput @updateTasks="updateTasks" />
        <div class="task-holder" v-for="task in tasks" :key="task.id">
          <TodoItem :task="task"/>
        </div>
    </div>
  </main>
</template>

<style scoped>
  main {
    display: flex;
    justify-content: center;
    align-items: center;
    height: auto;
    margin-top: 25vh;
  }  

  .list h1 {
    margin: 10px 0;
  }

  .list {
    display: flex;
    flex-direction: column;
    align-items: center;
    
    width: 50%;
    min-width: 400px;
    margin: auto;

    background-color: #ffffff;
    border-radius: 10px;
  }

  .task-holder{
    width: 100%;
    text-align: center;
  }
</style>