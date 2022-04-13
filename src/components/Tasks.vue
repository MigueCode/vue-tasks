<template>
  <div class="container">
    <h2>Create a new Task</h2>
    <CreateTask @task-created="sendData" />
    <h2>Tasks to do</h2>
    <Task :tasks="tasks" />
  </div>
</template>

<script>
import Task from "./Task.vue";
import CreateTask from "./CreateTask.vue";

export default {
  name: "Tasks",
  components: {
    Task,
    CreateTask,
  },

  data() {
    return {
      tasks: [],
    };
  },

  methods: {
    sendData(t) {
      console.log(t);

      fetch("https://api-tasks-dev.herokuapp.com/api/tasks", {
        method: "POST",
        body: JSON.stringify(t),
        headers: {
          "Content-type": "application/json; charset=UTF-8",
        },
      }).then(() => this.getData());

      t.task = "";
    },

    getData() {
      fetch("https://api-tasks-dev.herokuapp.com/api/tasks")
        .then((response) => response.json())
        .then((json) => (this.tasks = [...json]));
    },
  },

  created() {
    this.getData();
    // this.copyTasks = [...this.tasks];
    // this.tasks = this.getData();
    // console.log("created");
    // console.log(this.copyTasks);
  },
};
</script>

<style></style>
