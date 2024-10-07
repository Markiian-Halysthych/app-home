<template>
    <div class="section">
        <div class="section-title">
            <span>OUTBOX</span>
        </div>
        <div id="messages" :class="{dark: isActive}">
            <div class="outbox-messages">
                <span id="drafts" :class="{dark: isActive}"><a href="">Drafts</a></span>
                <span>14</span>
            </div>
            <div class="outbox-messages">
                <span class="failed-to-send"><a href="">Failed to send</a></span>
                <span class="failed-message-count">7</span>
            </div>
        </div>
      </div>
</template>

<script>
export default {
    name: 'OutboxComponent',
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
.outbox-messages {
    display: flex;
    justify-content: space-between;
    padding: 15px;
    padding-right: 0;
}
.outbox-messages a {
    text-decoration: none;
    color: black;
}
#drafts.dark a {
    color: white;
}
.failed-to-send a {
    color: red;
}
.failed-message-count {
    color: red;
}
</style>