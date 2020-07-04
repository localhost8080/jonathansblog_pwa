<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <h1 v-html="category.name"></h1>
          <router-link v-if="post.length > 0" class="btn btn-primary btn-block" v-bind:to="'/category/' + category.id">View Posts</router-link>
          <router-link v-if="cat.length > 0" class="btn btn-success btn-block" v-bind:to="'/category_list/' + category.id">View Sub Categories</router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'Category',
  props: ['category'],
  data(){
    return {
      post: [],
      cat: []
    }
  },
  mounted(){
    axios.get('https://jonathansblog.co.uk/wp-json/wp/v2/posts?categories=' + this.category.id)
    .then(response => {
      this.post = response.data
      console.log(response.data)
    }),
     axios.get('https://jonathansblog.co.uk/wp-json/wp/v2/categories?per_page=100&parent=' + this.category.id)
    .then(response => {
      this.cat = response.data
      console.log(response.cat)
    })  
  }
}
</script>

<style scoped>
h1 {
  margin: 40px 0 0;
}
</style>
