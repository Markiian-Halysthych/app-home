<template>
    <div class="search-bar-holder">
        <input class="search-bar" type="text" placeholder=" Search in App..." />
    </div>
</template>

<script>
export default {
    name: 'SearchBar'
}
</script>

<style scoped>
.search-bar-holder {
    margin-bottom: 10px;
    display: flex;
    justify-content: center;
    padding: 10px;
}
.search-bar {
    display: flex;
    border: none;
    border-radius: 5px;
    background-color: hsl(0, 0%, 88%);
    padding: 5px;
    width: 100%;
}
</style>