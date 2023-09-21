<script setup>
  import TodoList from './components/TodoList.vue';
  import TodoInput from './components/TodoInput.vue';
</script>

<template>
  <main>
    <div class="list">
      <h1>To-Do List</h1>
      <TodoInput/>
      <p>_____________________________</p>
      <TodoList/>
    </div>
  </main>
</template>

<style scoped>

  main {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }  

  .list h1 {
    margin: 10px 0;
  }

  .list {
    display: flex;
    flex-direction: column;
    align-items: center;
    
    width: 50%;
    margin: auto;

    background-color: #ffffff;
    border-radius: 10px;
  }
</style>