<template>
    <div class="container">
        <img src="https://khang.my.canva.site/2/videos/a88137ee1405f912a3332c468b7aedc4.gif" alt="">

        <div class="ad">
            <h1>VÀ VIDEO DỰ ÁN CUỐI CÙNG...</h1>
            <p>Stay tune, we promise it will be worth it</p>
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
        grid-area: d;

        font-size: 85px;
        height: max-content;
    }

}

img {
    position: relative;

    width: 100%;
    max-width: 400px;
    height: 100%;
    object-fit: cover;

}


@media screen and (max-width: 850px) {
    .container {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
}
</style>