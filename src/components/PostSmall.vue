<template>
  <div>
    <img class="img-fluid" :src="post.jetpack_featured_media_url">
    <h1 v-html="post.title.rendered"></h1>
    <div v-html="post.excerpt.rendered"></div>
    <router-link class="btn btn-success" v-bind:to="'/post/' + post.id">View more</router-link>
  </div>
</template>

<script>
export default {
  name: 'PostSmall',
  props: ['post']
}
</script>

<style scoped>
h1 {
  margin: 40px 0 0;
}
</style>
