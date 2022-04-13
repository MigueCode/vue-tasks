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

<style></style>
