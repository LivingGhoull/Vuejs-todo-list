<script setup>
  import TodoItem from './components/TodoItem.vue';
  import TodoInput from './components/TodoInput.vue';
  import { ref } from 'vue';

  let tasks = ref([]) 

  const UpdateTasks = (newTasks) => { tasks.value = newTasks }
  const RemoveTask = (index) => { tasks.value.splice(index, 1) }
</script>

<template>
  <main>
    <div class="list">
      <h1>To-Do List</h1>
      <TodoInput @updateTasks="UpdateTasks" />
        <div class="task-holder" v-for="(task, i) in tasks" :key="task.id">
          <TodoItem @remove="RemoveTask(i)" :task="task"/>
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