<template>
  <div class="mb-4">
    <img class="img-fluid" :src="post.jetpack_featured_media_url">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <h4 class="mt-2" v-html="post.title.rendered"></h4>
          <div v-html="post.excerpt.rendered"></div>
          <router-link class="btn btn-primary btn-block" v-bind:to="'/post/' + post.id">View more</router-link>
        </div>
      </div>
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
