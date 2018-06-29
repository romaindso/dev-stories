<template>
  <div id="app">
    <h1>Dev stories</h1>
    <story></story>
  </div>
</template>

<script>
import data from "./data";
import Story from "./Story.vue";

export default {
  name: "app",

  components: {
    story: Story
  }
};
</script>

<style lang="scss">
html,
body {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: #42b983;
  background-color: #2c3e50;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

#app > h1 {
  font-family: "Lobster", cursive;
  color: white;
  font-size: 150px;
  margin-top: 0;
}
</style>
