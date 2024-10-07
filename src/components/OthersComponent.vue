<template>
    <div class="section">
        <div class="section-title">
            <span>OTHERS</span>
        </div>
        <div id="messages" :class="{dark: isActive}">
            <div class="other-messages" :class="{dark: isActive}">
                <span><a href="">Favorites</a></span>
            </div>
            <div class="other-messages" :class="{dark: isActive}">
                <span><a href="">Spaces</a></span>
            </div>
            <div class="other-messages" :class="{dark: isActive}">
                <span><a href="">History</a></span>
            </div>
        </div>
      </div>
</template>

<script>
export default {
    name: 'OthersComponent',
    data() {
    return {
      isActive: false
    };
  },
  computed: {
    themeSitch(){
      return this.isActive ? 'message a' : 'message-dark a';
    }
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
.section {
    padding: 10px;
}
.section-title {
    margin-bottom: 10px;
    font-size: small;
}
#messages {
    border-radius: 5px;
    padding: 10px;
    background-color: white;
    transition: background-color 0.5s ease;
}
#messages.dark {
    background-color: #18263E;
}
.other-messages {
    display: flex;
    justify-content: space-between;
    padding: 15px;
    padding-right: 0;
}
.other-messages a {
    text-decoration: none;
    color: black;
}
.other-messages.dark a {
    color: white;
}
</style>