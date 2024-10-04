<template>
  <div id="app">
    <Header></Header>
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style scoped>
#app{
  font-family: Arial, Helvetica, sans-serif;
  padding: 10px;
}
</style>
