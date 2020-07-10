<template>
  <div id="app">
    <transition name="fade" mode="out-in">
      <router-view />
    </transition>
    <div class="row">
        <div class="col-12">
        <div id="nav" class="navbar fixed-bottom navbar-light bg-light">
          <router-link class="navbar-brand" to="/"><font-awesome-icon icon="home"></font-awesome-icon></router-link>
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
.container {
  overflow:hidden;
}
.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0
}

.btn.btn-primary, .btn.btn-primary:not(:disabled):not(.disabled):active{
  background:#008582;
  border:#008582;
}
</style>
