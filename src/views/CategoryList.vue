<template>
  <div class="home">
       <Category 
      v-for="category in categories"
      v-bind:key="category.id"
      v-bind:category="category"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Category from '@/components/Category.vue'
import axios from 'axios'

export default {
  name: 'categories',
  data(){
    return {
      categories: []
    }
  },
   components: {
    Category
  },
    mounted(){
    axios.get('https://jonathansblog.co.uk/wp-json/wp/v2/categories?per_page=100&parent=' + this.$route.params.id )
    .then(response => {
      this.categories = response.data
      // console.log(response.data)
    })
  }
}
</script>
