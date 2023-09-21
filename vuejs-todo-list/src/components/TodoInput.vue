<script setup>
</script>

<template>
  <div class="create-task">
    <input type="text" placeholder="Write a task!">
    <button>Submit</button>
  </div>
</template>

<style scoped>
  .create-task {
    display: flex;
    justify-content: center;
    width: 100%;
    gap: 20px;
    margin: 5%;
  }

  .create-task button{
    background-color: rgba(49,118,208,1);
    color: #ffffff;
    border: none;
    border-radius: 5px;
    padding: 10px 20px;
  }

  .create-task input{
    flex-shrink: 0;
    padding: 0 10px;
    border: 1px solid rgb(150, 150, 150);
    border-radius: 5px;
  }
</style>