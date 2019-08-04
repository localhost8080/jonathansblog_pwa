<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <PostSmall 
      v-for="post in posts"
      v-bind:key="post.id"
      v-bind:post="post"/>
  </div>
</template>

<script>
// @ is an alias to /src
import axios from 'axios'
import PostSmall from '@/components/PostSmall.vue'


export default {
  name: 'category_id',
  data(){
    return {
      posts: []
    }
  },
  components: {
    PostSmall
  },
    mounted(){
    axios.get('https://jonathansblog.co.uk/wp-json/wp/v2/posts?categories=' + this.$route.params.id)
    .then(response => {
      this.posts = response.data
      console.log(response.data)
    })
    
  }
}
</script>
