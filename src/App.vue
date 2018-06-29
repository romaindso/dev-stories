<template>
  <div id="app">
    <div>
      <h1>Dev stories</h1>
      <story></story>
    </div>
    <footer>
      <a href="https://github.com/romaindso/dev-stories/pulls" target="_blank">Soumettre une story</a>
    </footer>
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

#app > div > h1 {
  font-family: "Lobster", cursive;
  color: white;
  font-size: 100px;
}

footer {
  position: sticky;
  top: 0;
}

footer a {
  color: white;
  font-style: italic;
}
</style>
