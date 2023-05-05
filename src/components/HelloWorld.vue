<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ul>
      <li v-for="post in posts" :key="post.id">
        <p>{{ post.text }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
import sourceData from '@/data.json';
console.log(sourceData);

export default {
  name: 'HelloWorld',
  data() {
    return {
      posts: sourceData.posts,
      users: sourceData.users
    }
  },
  props: {
    msg: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
