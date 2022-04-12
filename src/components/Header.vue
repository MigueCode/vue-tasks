<template>
  <div class="header">
    <h1>{{ msg }}</h1>
    <p>
      Checkout My Web<br />
      <a href="https://miguecode.github.io/cv/" target="_blank" rel="noopener"
        >Luis Miguel Developer</a
      >
    </p>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
