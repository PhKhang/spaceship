<template>
    <div class="container">
        <img id="cau" src="@/assets/caugiay.png" alt="">
        <img id="えー等" src="@/assets/docえー等.png" alt="">
        <img id="エー等" src="@/assets/エー等.jpg" alt="">
        <img id="bts" src="@/assets/sauquayphim.png" alt="">
        <img id="quayphim" src="@/assets/quayphim.png" alt="">
        <div class="heading">
            <h1>CÁC DỰ ÁN:</h1>
            <p>Từ cầu giấy, mindmap đến dựng phim và hơn thế nữa...</p>
        </div>



    </div>
</template>

<script>

</script>

<style lang="scss" scoped>
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);
    grid-template-areas:
        "a a b"
        "d e b"
        "c c b";

    gap: 20px;

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

    #cau {
        grid-area: a;
    }

    #えー等 {
        grid-area: b;
    }

    #エー等 {
        display: none;
    }

    #bts {
        grid-area: c;
    }

    #quayphim {
        grid-area: e;
    }

}

img {
    position: relative;

    width: 100%;
    height: 100%;
    object-fit: cover;

    &:hover {
        transform: scale(1.05);
    }
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

    img {
        pointer-events: none;
    }

    #えー等 {
        display: none;
    }

    #エー等 {
        display: unset;
        grid-area: b;
    }
}
</style>