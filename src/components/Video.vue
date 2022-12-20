<template>
    <div class="container">
        <img src="@/assets/poster.png" alt="">

        <div class="ad">
            <h1>VÀ VIDEO DỰ ÁN CUỐI CÙNG...</h1>
            <p><a href="https://youtu.be/Vx8GBkIcbA0">youtu.be/Vx8GBkIcbA0</a></p>
        </div>
    </div>
</template>

<script>

</script>

<style lang="scss" scoped>
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    width: 100%;
    max-width: 1200px;
    height: max-content;
    padding: 0 10px 0 10px;


    position: relative;
    left: 50%;
    transform: translate(-50%);


    h1 {
        font-size: 85px;
        height: max-content;
    }

    a {
        text-decoration: underline;
        color: inherit;
    }

}

img {
    position: relative;

    width: 100%;
    max-width: 400px;
    height: 100%;
    object-fit: cover;

    margin: 10px;
    border-radius: 15px;


}


@media screen and (max-width: 850px) {
    .container {
        display: flex;
        flex-direction: column-reverse;
        gap: 20px;

        h1 {
            font-size: 60px;
        }
    }

}
</style>