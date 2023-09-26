<script setup>
  import { reactive } from 'vue';
  let taskMessege = ''
  let listOfTasks = reactive([])
  let index = 0

  const emit = defineEmits(['customChange'])

  const CreateTask = () => {  
    listOfTasks.push({
      id: index++,
      task: taskMessege,
      complete: false
    })
    emit('updateTasks', listOfTasks)  
  }
</script>

<template>
  <div class="create-task">
    <input v-model="taskMessege" type="text" placeholder="Write a task!">
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
    border: 1px solid rgb(28, 91, 174);
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