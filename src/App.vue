<template>
  <div id="app">
      <div id="nav" class="navbar navbar-light bg-light">
        <router-link class="navbar-brand" to="/">Home</router-link>
        <router-link class="navbar-brand" to="/category_list/0">Categories</router-link>
      </div>

      <router-view />
  </div>
</template>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
h1 {
  text-align:center
}
</style>
