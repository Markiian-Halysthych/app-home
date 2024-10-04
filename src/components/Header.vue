<template>
  <header class="header">
    <div class="title">Hub Cockpit</div>
    <button class="add-button">+ New</button>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-self: center;
  padding: 10px;
  margin-bottom: 10px;
  /* border-radius: 10px; */
}
</style>
