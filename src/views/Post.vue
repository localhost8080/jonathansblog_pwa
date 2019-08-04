<template>
  <div class="home">
    <img class="img-fluid" :src="post.jetpack_featured_media_url"> 
    <h1 v-html="post.title.rendered"></h1>
    <div v-html="post.content.rendered"></div>
  </div>
</template>

<script>
// @ is an alias to /src
import axios from 'axios'

export default {
  name: 'post',
  data(){
    return {
      post: []
    }
  },
    mounted(){
    axios.get('https://jonathansblog.co.uk/wp-json/wp/v2/posts/' + this.$route.params.id)
    .then(response => {
      this.post = response.data
      console.log(response.data)
    })
    
  }
}
</script>
