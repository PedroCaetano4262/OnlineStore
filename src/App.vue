<template>
  <Home msg="Welcome to Your Vue.js App"/>
</template>

<script>
import Home from './components/HelloWorld.vue'


export default {
  name: 'App',
  components: {
    Home,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  background-image: url("img-1719570668998.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
