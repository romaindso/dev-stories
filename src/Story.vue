<template>
  <blockquote>
    <h1>{{ story.text }}</h1>
    <span>- {{ story.author }}</span>
  </blockquote>
</template>

<script>
import data from './data'

export default {
  name: 'story',

  data () {
    return {
      story: data.stories[Math.floor(Math.random() * data.stories.length)]  
    }
  }
}
</script>

<style lang="scss">
blockquote {
  width: 800px;
  margin: 0 auto;

  h1 {
    font-family: 'Lobster', cursive;
    font-size: 40px;
    font-weight: 400;
    padding-left: 15px;
    border-left: 1px solid #42b983;
    text-align: left;

    &::before, &::after {
      content: '" ';
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