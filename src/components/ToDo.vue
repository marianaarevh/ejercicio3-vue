<template>
    <div>
      <h1>To-Do List</h1>
      <div class="task-input">
        <input v-model="newTask" @keyup.enter="addTask" placeholder="add task" />
        <button id="addTask" @click="addTask">+</button>
      </div>
      <div class="tasks-container">
        <table id="data-table">
          <thead>
            <tr>
              <th>Task</th>
              <th>Eliminar</th>
            </tr>
          </thead>
          <tbody id="data-table-body">
            <tr v-for="(task, index) in tasks" :key="index">
                <td>{{ task }}</td>
                <td>
                    <button id="removeTask" @click="removeTask(index)">x</button>
                </td>
            </tr>
         </tbody>
        </table>
      
    </div>
    </div>
  </template>

<script>
export default {
  data() {
    return {
      newTask: "",
      tasks: []
    };
  },
  methods: {
    addTask() {
        this.tasks.push(this.newTask);
        this.newTask = "";
    },

    removeTask(index) {
      this.tasks.splice(index, 1);
    }
  }
};
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

#removeTask{
    width: 40px;
    font-size: 1rem;
    margin: 5px;
    font-size: 600;
    color: red;

}

.tasks-container{
    max-width: 100%;
    overflow-x: auto;
    margin: 10px;
    border-radius: 10px;
} 
  
  table {
    width: 100%;
    border-collapse: collapse;
    white-space: nowrap;
    font-size: 1rem;
  }

  th {
    padding: 15px;
    background-color: rgb(244, 244, 241);
    color: black;
  }

  tbody td {
    white-space: wrap;
    background-color: rgba(244, 244, 241, 0.343);
  }


</style>