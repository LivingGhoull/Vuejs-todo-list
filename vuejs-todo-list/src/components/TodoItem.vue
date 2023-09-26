<script setup>


const deleteTask = () => {
  console.log('test');
}

</script>

<template>
  <div class="task">
    <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
    <label for="vehicle1">task</label>
    <button @click="deleteTask">Delete</button>
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

.task input {
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