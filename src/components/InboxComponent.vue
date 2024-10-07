<template>
    <div class="section">
        <div class="section-title">
            <span>INBOX</span>
        </div>
        <div id="messages" :class="{dark: isActive}">
            <div class="unseen-messages">
                <span>All unseen messages</span>
                <span class="message-count">14</span>
            </div>
            <div class="messages-list">
                <div class="message" :class="{dark: isActive}">
                    <span>
                        <a href="">
                            <img class="messages-icon" :src="getImage('emails')"> 
                            E-mails
                        </a>
                    </span>
                    <span>3</span>
                </div>
                <div class="message" :class="{dark: isActive}">
                    <span>
                        <a href="">
                            <img class="messages-icon" :src="getImage('teams')"> 
                            MS Teams
                        </a>
                    </span>
                    <span>7</span>
                </div>
                <div class="message" :class="{dark: isActive}">
                    <span>
                        <a href="">
                            <img class="messages-icon" src="@/assets/slack.png"> 
                            Slack
                        </a>
                    </span>
                    <span>2</span>
                </div>
                <div class="message" :class="{dark: isActive}">
                    <span>
                        <a href="">
                            <img class="messages-icon" src="@/assets/whatsApp.png"> 
                            WhatsApp
                        </a>
                    </span>
                    <span>2</span>
                </div>
            </div>
        </div>
      </div>
</template>

<script>
export default {
    name: 'InboxCoomponent',
    data() {
    return {
      isActive: false,
      images: {
        light: {
            emails: require('@/assets/post.png'),
            teams: require('@/assets/teams.png'),
        },
        dark: {
            emails: require('@/assets/postDark.png'),
            teams: require('@/assets/teamsDark.png'),
        }
      }
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
  methods: {
    getImage(service) {
        return this.isActive ? this.images.dark[service] : this.images.light[service];
    }
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
.unseen-messages {
    display: flex;
    justify-content: space-between;
    padding: 5px;
    padding-right: 0;
}
.messages-list {
    padding-left: 8px;
}
.message {
    padding: 10px;
    padding-right: 0;
    display: flex;
    justify-content: space-between;
}
.message a {
    text-decoration: none;
    color: black
}
.message.dark a {
    color: white;
}
.messages-icon {
    max-width: 17px;
    height: auto;
}
</style>