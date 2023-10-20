<template>
    <div>
      <h1>To-Do List</h1>
      <div class="task-input">
        <input v-model="newTask" @keyup.enter="addTask" placeholder="add task" />
        <button id="addTask" @click="addTask">+</button>
      </div>
      <ul>
        <li v-for="(task, index) in tasks" :key="index">
          {{ task }}
          <button @click="removeTask(index)">Eliminar</button>
        </li>
      </ul>
    </div>
  </template>

<script>
export default {
  name: 'ToDo'
}
</script>

<style>
input{
    padding: 10px;
    margin: 10px;
    font-size: 1.2rem;
    border-radius: 20px;
}

#addTask{
    background-color: green;
}

ul{

}

li{
    
}
</style>