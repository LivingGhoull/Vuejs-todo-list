<script setup>

const CreateTask = () => { 
  console.log('hello');
}

</script>

<template>
  <div class="create-task">
    <input type="text" placeholder="Write a task!">
    <button @click="CreateTask">Submit</button>
  </div>
</template>

<style scoped>
  .create-task {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin: 5% 0;
  }

  .create-task button{
    background-color: rgba(49,118,208,1);
    color: #ffffff;
    border: none;
    border-radius: 5px;
    padding: 10px 20px;
    cursor: pointer;
    transition: background-color 300ms ease;
  }
  
  .create-task button:hover {
    background-color: rgb(28, 91, 174);
  }


  .create-task input{
    padding: 0 10px;
    border: 1px solid rgb(150, 150, 150);
    border-radius: 5px;
  }
</style>