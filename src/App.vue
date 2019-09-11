<template>
  <div id="app">
    <blog-post title="My journey with Vue" size="8"></blog-post>
    <blog-post title="Blogging with Vue"></blog-post>
    <blog-post title="Why Vue is so fun"></blog-post>
    <p>--------------------------------------------------</p>
    <blog-post
      v-for="post in posts"
      v-bind:key="post.id"
      v-bind:title="post.title"
      v-bind:size="post.size">
    </blog-post>
    <p>--------------------------------------------------</p>
    <ButtonCounter></ButtonCounter>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import ButtonCounter from './components/ButtonCounter.vue'
import BlogPost from './components/BlogPost.vue'

export default {
  name: 'app',
  components: {
    //HelloWorld,
    BlogPost,
    ButtonCounter
  },
  data: function() {
    return {
      posts: [
        { id: 1, title: 'My journey with Vue', size: '8' },
        { id: 2, title: 'Blogging with Vue', size: '9' },
        { id: 3, title: 'Why Vue is so fun', size: '10' },
        { id: 4, title: 'Who fun with you?', size: '12' },
        { id: 5, title: 'Me!! Maybe?', size: '13' },
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
