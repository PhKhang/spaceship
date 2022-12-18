<template>
    <nav>
        <router-link to="/"><img src="@/assets/dark.png" alt=""></router-link>
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
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: space-between;

    position: fixed;
    top: 0;
    left: 0;
    z-index: 9;

    padding: 10px;

    color: #637990;
    background-color: rgba(0, 0, 0, 0.518);
    backdrop-filter: blur(50px);

    img {
        height: 50px;
        object-fit: cover;
    }

    a {
        font-weight: bold;
        margin: auto;
        color: #637990;

        &.router-link-exact-active {
            color: white;
            text-decoration: underline;
        }
    }
}
</style>