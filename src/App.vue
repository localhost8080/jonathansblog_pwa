<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <router-view />
        </div>
      </div>
      <div class="row">
         <div class="col-12">
          <div id="nav" class="navbar fixed-bottom navbar-light bg-light">
            <router-link class="navbar-brand" to="/"><font-awesome-icon icon="home"></font-awesome-icon></router-link>
            <router-link class="navbar-brand" to="/category_list/0"><font-awesome-icon icon="bars"></font-awesome-icon></router-link>
          </div>
        </div>
      </div>
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
