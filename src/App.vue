<template>
  <div id="app">
    <div class="navbar-fixed">
      <nav>
        <div class="nav-wrapper">
          <a href="#!" class="brand-logo center">Identicon Generator</a>
        </div>
      </nav>
    </div>
    <Identicon />
  </div>
</template>

<script>
import Identicon from "./components/Identicon.vue";

export default {
  name: "app",
  components: {
    Identicon
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  background-color: black;
}
</style>
