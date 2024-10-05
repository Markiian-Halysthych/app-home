<template>
    <div class="section">
        <div class="section-title">
            <span>OTHERS</span>
        </div>
        <div class="messages">
            <div class="other-messages">
                <span><a href="">Favorites</a></span>
            </div>
            <div class="other-messages">
                <span><a href="">Spaces</a></span>
            </div>
            <div class="other-messages">
                <span><a href="">History</a></span>
            </div>
        </div>
      </div>
</template>

<script>
export default {
    name: 'OthersComponent'
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
</style>