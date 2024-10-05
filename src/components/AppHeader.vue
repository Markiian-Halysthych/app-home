<template>
  <header class="header">
    <div class="title"><img class="logo-img" src="@/assets/logo.png"/> Hub Cockpit</div>
    <button class="add-button">+ New</button>
  </header>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-self: center;
  padding: 10px;
  margin-bottom: 10px;
}

.title{
  font-size: 20px;
  font-weight: bold;
}

.add-button{
  border-radius: 5px;
  border: none;
  background-color: #3172D5;
  color: white;
}

.add-button:hover{
  background-color: #245db3;
}
.logo-img {
  max-width: 17px;
  height: auto;
}
</style>
