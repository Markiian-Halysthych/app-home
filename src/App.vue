<template>
  <div id="app">
    <AppHeader></AppHeader>
    <AppSearchBar></AppSearchBar>
    <InboxComponent></InboxComponent>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppSearchBar from './components/SearchBar.vue';
import InboxComponent from './components/InboxComponent.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppSearchBar,
    InboxComponent,
  }
}
</script>

<style scoped>
#app{
  font-family: Arial, Helvetica, sans-serif;
  padding: 10px;
}
</style>
