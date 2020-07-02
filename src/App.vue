<template>
  <div id="app">
    <!-- <Count /> -->
    <ImprintOption combinationsText="werwer" :callback="testEvent" />
  </div>
</template>

<script>
import Count from './components/Count/Count'
import ImprintOption from './components/ImprintOption/ImprintOption'
export default {
  name: 'App',
  components: { Count, ImprintOption },
  methods: {
    testEvent() {
      console.log('test test')
    }
  }
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
