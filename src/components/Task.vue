<template>
  <div class="task-container" v-for="task in tasks" :key="task.id">
    <div>
      <input type="checkbox" name="" id="" />
      <span>{{ task.task }}</span>
    </div>
    <div>
      <button>Edit</button>
      <button>Delete</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tasks: Array,
  },
};
</script>

<style>
.task-container {
  width: 280px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}
</style>
