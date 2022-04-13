<template>
  <input v-model="task.task" placeholder="Add your task to do" />
  <button @click="$emit('taskCreated', this.task)">Create</button>
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

  methods: {},
};
</script>

<style scoped>
input {
  width: 240px;
  height: 30px;
  border-radius: 10px;
  border: none;
  background-color: rgb(208, 253, 253);
  padding: 5px;
  outline-style: none;
  font-size: 16.5px;
}

input::placeholder {
  font-size: 16.5px;
}

button {
  margin-left: 8px;
  height: 30px;
  width: 75px;
  background-color: blue;
  border: none;
  border-radius: 8px;
  color: white;
  font-size: 16.5px;
  cursor: pointer;
}
</style>
