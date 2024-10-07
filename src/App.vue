<template>
  <div id="app" :class="{dark: isActive}">
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
  },
  data() {
    return {
      isActive: false
    };
  },
  methods: {
    toggleStyle() {
      this.isActive = !this.isActive;
    }
  },
  provide() {
    return {
      isActive: this.$data.isActive,
      toggleStyle: this.toggleStyle
    }
  },
  watch: {
    isActive(newValue) {
      this.$root.$emit('toggle-style', newValue);
    }
  }
}
</script>

<style scoped>

#app {
  font-family: Arial, Helvetica, sans-serif;
  background-color: hsl(0, 0%, 96%);
  min-height: 100vh;
  transition: background-color 0.5s ease;
  padding-bottom: 7vh;
}
#app.dark {
  background-color: hsl(219, 68%, 10%);
  color: white;
}
</style>
