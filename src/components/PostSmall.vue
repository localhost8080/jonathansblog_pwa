<template>
  <div class="card mb-4">
    <img class="card-img-top img-fluid" :src="post.jetpack_featured_media_url">
      <div class="card-body">
        <h4 class="card-title mt-2" v-html="post.title.rendered"></h4>
        <div v-html="post.excerpt.rendered"></div>
        <router-link class="btn btn-primary btn-block" v-bind:to="'/post/' + post.id">View more</router-link>
      </div>
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
