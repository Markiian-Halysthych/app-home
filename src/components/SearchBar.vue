<template>
    <div class="search-bar-holder">
        <input id="search-bar" :class="{dark: isActive}" type="text" placeholder=" Search in App..." />
    </div>
</template>

<script>
export default {
    name: 'SearchBar',
    data() {
    return {
      isActive: false
    };
  },
  mounted() {
    this.$root.$on('toggle-style', (status) => {
      this.isActive = status;
    })
  },
  inject: ['toggleStyle'],
}

</script>

<style scoped>
.search-bar-holder {
    margin-bottom: 10px;
    display: flex;
    justify-content: center;
    padding: 10px;
}
#search-bar {
    display: flex;
    border: none;
    border-radius: 5px;
    background-color: hsl(0, 0%, 88%);
    padding: 5px;
    width: 100%;
}
#search-bar.dark {
    background-color: hsl(219, 68%, 10%);
    border: 0.5px solid white;
}
#search-bar.dark::placeholder {
    color: #DEE5EF;
}
</style>