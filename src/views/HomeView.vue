<template>
  <div class="home">
    <img alt="App logo" src="../assets/logo.png" />
    <Header msg="Welcome to Your Tasks to Do App" />
    <Tasks />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header.vue";
import Tasks from "@/components/Tasks.vue";

export default {
  name: "HomeView",
  components: {
    Header,
    Tasks,
  },
};
</script>

<style scoped>
img {
  max-width: 180px;
  height: auto;
}
</style>
