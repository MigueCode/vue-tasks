<template>
  <input v-model="task.task" placeholder="Add your task to do" />
  <button @click="sendData">Create</button>
</template>

<script>
export default {
  data() {
    return {
      task: {
        task: "",
      },
    };
  },

  methods: {
    sendData() {
      console.log(this.task);

      fetch("https://api-tasks-dev.herokuapp.com/api/tasks", {
        method: "POST",
        body: JSON.stringify(this.task),
        headers: {
          "Content-type": "application/json; charset=UTF-8",
        },
      }).then((res) => console.log(res));

      this.task.task = "";
    },
  },
};
</script>

<style></style>
