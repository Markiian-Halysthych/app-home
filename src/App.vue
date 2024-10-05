<template>
  <div id="app">
    <AppHeader></AppHeader>
    <AppSearchBar></AppSearchBar>
    <InboxComponent></InboxComponent>
    <OutboxComponent></OutboxComponent>
    <OthersComponent></OthersComponent>
    <BottomNav></BottomNav>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppSearchBar from './components/SearchBar.vue';
import InboxComponent from './components/InboxComponent.vue';
import OutboxComponent from './components/OutboxComponent.vue';
import OthersComponent from './components/OthersComponent.vue';
import BottomNav from './components/BottomNav.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppSearchBar,
    InboxComponent,
    OutboxComponent,
    OthersComponent,
    BottomNav,
  }
}
</script>

<style scoped>
#app{
  font-family: Arial, Helvetica, sans-serif;
}
</style>
