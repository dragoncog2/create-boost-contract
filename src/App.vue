<template>
  <Main />
</template>

<script>
import main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Main: main
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 100px;
}
</style>
