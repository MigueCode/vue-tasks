<template>
  <div class="task-container" v-for="task in tasks" :key="task._id">
    <div>
      <input type="checkbox" name="" id="" />
      <span>{{ task.task }}</span>
    </div>
    <div class="btn-div">
      <button @click="$emit('taskDel', task._id)">Delete</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tasks: Array,
  },

  /* data() {
    return {
      ev =
    };
  }, */

  methods: {},
};
</script>

<style>
.task-container {
  width: 280px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  margin-bottom: 4px;
  text-align: left;
}

.btn-div {
  padding-left: 6px;
}

span {
  font-size: 17px;
}

button {
  font-size: 15px;
  height: 25px;
  width: 70px;
  background-color: rgb(255, 0, 0);
  border: none;
  border-radius: 8px;
  color: white;
  cursor: pointer;
}
</style>
