<template>
  <div id="app">
    <shape-outside></shape-outside>
  </div>
</template>

<script>
import shapeOutside from '@/views/cssExamples/shapeOutside/index'

export default {
  name: 'App',
  components: {
    shapeOutside
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
