<template>
    <div class="section">
        <div class="section-title">
            <span>INBOX</span>
        </div>
        <div class="messages">
            <div class="unseen-messages">
                <span>All unseen messages</span>
                <span class="message-count">14</span>
            </div>
            <div class="messages-list">
                <div class="message">
                    <span><a href=""><img class="messages-icon" src="@/assets/post.png"> E-mails</a></span>
                    <span>3</span>
                </div>
                <div class="message">
                    <span><a href=""><img class="messages-icon" src="@/assets/teams.png"> MS Teams</a></span>
                    <span>7</span>
                </div>
                <div class="message">
                    <span><a href=""><img class="messages-icon" src="@/assets/slack.png"> Slack</a></span>
                    <span>2</span>
                </div>
                <div class="message">
                    <span><a href=""><img class="messages-icon" src="@/assets/whatsApp.png"> WhatsApp</a></span>
                    <span>2</span>
                </div>
            </div>
        </div>
      </div>
</template>

<script>
export default {
    name: 'InboxCoomponent'
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
.messages {
    border-radius: 5px;
    padding: 10px;
    background-color: white;
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
.messages-icon {
    max-width: 17px;
    height: auto;
}
</style>