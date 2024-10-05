<template>
    <div class="section">
        <div class="section-title">
            <span>OUTBOX</span>
        </div>
        <div class="messages">
            <div class="outbox-messages">
                <span><a href="">Drafts</a></span>
                <span>14</span>
            </div>
            <div class="outbox-messages">
                <span class="failed-to-send"><a href="">Failed to send</a></span>
                <span class="message-count">7</span>
            </div>
        </div>
      </div>
</template>

<script>
export default {
    name: 'OutboxComponent'
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
.failed-to-send a {
    color: red;
}
.message-count {
    color: red;
}
</style>