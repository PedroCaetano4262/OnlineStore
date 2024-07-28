<template>
  <Home msg="Welcome to Your Vue.js App"/>
</template>

<script>
import Home from './components/HelloWorld.vue'
import RegisterForm from './components/RegisterForm.vue'

export default {
  name: 'App',
  components: {
    Home,
    RegisterForm
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
</style>
