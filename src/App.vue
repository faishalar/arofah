<template>
  <div id="app">
    <navigasi></navigasi>
  </div>
</template>

<script>
import Navigasi from './components/Navigasi.vue'

export default {
  name: 'App',
  components: {
    Navigasi
  }
}
</script>

<style>
*{
  margin-top:0;
  padding:0;
}
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

</style>
