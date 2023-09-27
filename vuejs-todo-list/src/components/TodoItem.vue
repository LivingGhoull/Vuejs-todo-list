<script setup>
  import { reactive, ref } from 'vue';

const props = defineProps(['task'])
const id = props.task.id
const messege = props.task.task
let complete = ref(props.task.complete)

const taskComplete = () => { 
  complete.value = !complete.value
}
</script>

<template>
  <div class="task">
    <div>
      <input @click="taskComplete" type="checkbox" :id="id" name="vehicle1" value="Bike">
      <label :class="{done: complete }" :for="id">{{ messege }}</label>
    </div>
    <button @click="$emit('remove')">Delete</button>
  </div>
</template>

<style scoped>
.task {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 40px;
  padding: 10px 0;
}

.task .done {
  text-decoration: line-through;
  color: gray;
}

.task button{
  background-color: rgb(238, 86, 60);
  color: #ffffff;
  border: 1px solid rgb(197, 23, 63);
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
  transition: background-color 300ms ease;
}

.task button:hover{
  background-color: rgb(197, 23, 63);
}
</style>