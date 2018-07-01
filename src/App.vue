<template>
  <div id="app">
    <header>
        <h1>Dev stories</h1>
      </header>
    <story></story>
    <footer>
      <a href="https://github.com/romaindso/dev-stories/pulls" target="_blank">Soumettre une story</a>
      <a href="https://github.com/romaindso/dev-stories/" class="button button-next">Next story</a>
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

header {
  position: relative;

  & > h1 {
    font-family: "Lobster", cursive;
    color: white;
    font-size: 100px;
    margin: 10px 0;
  }
}

footer {
  position: sticky;
  text-align: center;
  margin-top: 40px;

  a {
    color: white;
    font-style: italic;
  }
}

.button-next {
  margin-left: 20px;
}

a.button {
  display: inline-block;
  padding: 0.7em 1.4em;
  border-radius: 0.15em;
  box-sizing: border-box;
  text-decoration: none;
  font-family: "Avenir", sans-serif;
  text-transform: uppercase;
  font-weight: 400;
  color: #ffffff;
  background-color: #42b983;
  box-shadow: inset 0 -0.6em 0 -0.35em rgba(0, 0, 0, 0.17);
  text-align: center;
  position: relative;
}

a.button:active {
  top: 0.1em;
}

@media all and (max-width: 30em) {
   a.button {
    display: block;
    margin: 0.4em auto;
  }
}
</style>
