<template>
  <div id="app">
    <hello></hello>
    <grid></grid>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Grid from './components/Grid'

export default {
  name: 'app',
  components: {
    Hello, Grid
  }
}
</script>

<style>
#app {
  font-family: -apple-system, BlinkMacSystemFont, 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
