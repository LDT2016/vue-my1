<template>
  <div id="app">
    <!-- <Count /> -->
    <ImprintOption />
  </div>
</template>

<script>
import Count from './components/Count/Count'
import ImprintOption from './components/ImprintOption/ImprintOption'
export default {
  name: 'App',
  components: { Count, ImprintOption }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
