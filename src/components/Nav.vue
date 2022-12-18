<template>
    <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </nav>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
nav {
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 9;

    padding: 10px;

    background-color: rgba(0, 0, 0, 0.518);
    backdrop-filter: blur(50px);

    a {
        font-weight: bold;
        color: #2c3e50;

        &.router-link-exact-active {
            color: #42b983;
        }
    }
}
</style>