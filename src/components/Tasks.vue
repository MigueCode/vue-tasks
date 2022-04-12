<template>
  <div class="container">
    <h2>Create a new Task</h2>
    <CreateTask />
    <h2>Tasks to do</h2>
    <Task :tasks="tasks" @task-created="getData" />
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
    console.log("created");
    // console.log(this.copyTasks);
  },
};
</script>

<style></style>
