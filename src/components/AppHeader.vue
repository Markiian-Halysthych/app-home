<template>
  <header class="header">
    <div class="title" :class="{dark: isActive}"><img class="logo-img" :src="getImage('logo')"/> Hub Cockpit</div>
    <div>
      <button class="theme-button" :class="{dark: isActive}" @click="toggleStyle">{{ buttonLabel }}</button>
      <button class="add-button">+ New</button>
  </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      isActive: false,
      images: {
        light: {
          logo: require('@/assets/logo.png')
        },
        dark: {
          logo: require('@/assets/logoDark.png')
        }
      }
    };
  },
  computed: {
    buttonLabel() {
      return this.isActive ? 'Light Theme' : 'Dark Theme';
    }
  },
  mounted() {
    this.$root.$on('toggle-style', (status) => {
      this.isActive = status;
    })
  },
  methods: {
    getImage(service) {
        return this.isActive ? this.images.dark[service] : this.images.light[service];
    }
  },
  inject: ['toggleStyle'],
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-self: center;
  align-items: center;
  padding: 10px;
  margin-bottom: 10px;
}
.title{
  display: flex;
  font-size: 20px;
  font-weight: bold;
  align-items: center;
}
.add-button{
  border-radius: 5px;
  border: none;
  background-color: #3172D5;
  color: white;
  margin-left: 10px;
  height: 4vh;
}
.add-button:hover{
  background-color: #245db3;
}
.logo-img {
  max-width: 17px;
  height: auto;
  padding: 10px;
}
.theme-button {
  height: 4vh;
  border-radius: 5px;
  border: none;
  background-color: #000000;
  color: white;
  margin-left: 10px;
}
.theme-button.dark {
  background-color: white;
  color: black;
}
</style>
