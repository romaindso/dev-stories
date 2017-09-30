<template>
  <div id="app">
    <img src="./assets/logo.png">
    <blockquote>
      <h1>{{ story.text }}</h1>
      <span>- {{ story.author }}</span>
    </blockquote>
  </div>
</template>

<script>
import data from './data'

export default {
  name: 'app',
  data () {
    return {
      story: data.stories[Math.floor(Math.random() * data.stories.length)]  
    }
  }
}
</script>

<style lang="scss">
html, body {
  color: #42b983;
  background-color: #2c3e50;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}

blockquote {
  width: 950px;
  margin: 0 auto;

  h1 {
    font-size: 40px;
    font-style: italic;
    padding-left: 15px;
    border-left: 1px solid #42b983;
    text-align: left;

    &::before, &::after {
      content: '"';
    }
  }
  
  span {
    display: block;
    color: #ccc;
    font-size: 30px;
    text-align: left;
  }
}
</style>
