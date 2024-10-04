<template>
  <header class="header">
    <div class="title">Hub Cockpit</div>
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
</style>
