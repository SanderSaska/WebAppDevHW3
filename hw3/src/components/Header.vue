<template>
    <div class="header">
        <h1>Header</h1>
        <nav>
            <router-link to="/">Home</router-link> |
            <router-link to="/signup">Signup</router-link>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'header'
}
</script>

<style scoped>
div {
    display: flex;
    background-color: grey;
    flex-direction: column;
}
</style>