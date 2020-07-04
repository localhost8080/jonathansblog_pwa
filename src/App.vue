<template>
  <div id="app">
     <router-view />
      <div id="nav" class="navbar fixed-bottom navbar-light bg-light">
        <router-link class="navbar-brand" to="/"><font-awesome-icon icon="home"></font-awesome-icon></router-link>
        <router-link class="navbar-brand" to="/category_list/0"><font-awesome-icon icon="bars"></font-awesome-icon></router-link>
      </div>

     
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
