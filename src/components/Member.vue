<template>
    <div class="container">
        <h1>THÀNH VIÊN</h1>

        <div class="member">
            <img src="@/assets/quanghuy.jpg" style="object-position: center 40%" alt="">
            <div class="info">
                <h2>01</h2>
                <h3>Nguyễn Quang Huy<br />Leader</h3>
                <p>MSSV: 22127157<br />Mail: nqhuy22@clc.fitus.edu.vn<br />FB: <a
                        href="https://www.facebook.com/profile.php?id=100024148426316">facebook.com/profile.php?id=100024148426316</a>
                </p>
            </div>
        </div>

        <div class="member">
            <img src="@/assets/thienbao.jpg" style="object-position: center 30%" alt="">
            <div class="info">
                <h2>02</h2>
                <h3>Nguyễn Thiên Bảo<br />Phó Leader</h3>
                <p>MSSV: 22127032<br />Mail: ntbao22@clc.fitus.edu.vn<br />FB: <a
                        href="facebook.com/thiennbao.204">facebook.com/thiennbao.204</a></p>
            </div>
        </div>

        <div class="member">
            <img src="@/assets/phuckhang.png" style="object-position: center 40%" alt="">
            <div class="info">
                <h2>03</h2>
                <h3>Trần Nguyễn Phúc Khang<br />Member</h3>
                <p>MSSV: 22127182<br />Mail: tnpkhang22@clc.fitus.edu.vn<br />FB: <a
                        href="https://www.facebook.com/PhKhng">facebook.com/PhKhng</a></p>
            </div>
        </div>

        <div class="member">
            <img src="@/assets/chitai.jpg" style="object-position: center 40%" alt="">
            <div class="info">
                <h2>04</h2>
                <h3>Lâm Chí Tài<br />Member</h3>
                <p>MSSV: 22127370<br />Mail: lctai22@clc.fitus.edu.vn<br />FB: <a
                        href="https://www.facebook.com/chitailam0101">facebook.com/chitailam0101</a></p>
            </div>
        </div>

        <div class="member">
            <img src="@/assets/ngocchau.jpg" alt="">
            <div class="info">
                <h2>05</h2>
                <h3>Ngọc Châu<br />Member</h3>
                <p>MSSV: 22127044<br />Mail: nqhuy22@clc.fitus.edu.vn<br />FB: <a
                        href="https://www.facebook.com/d18.is.real">facebook.com/d18.is.real</a></p>
            </div>
        </div>

        <div class="member">
            <img src="@/assets/minhhuy.jpeg" alt="">
            <div class="info">
                <h2>06</h2>
                <h3>Đỗ Minh Huy<br />Member</h3>
                <p>MSSV: 22127147<br />Mail: dmhuy22@clc.fitus.edu.vn<br />FB: <a
                        href="https://www.facebook.com/profile.php?id=100045360666811">facebook.com/profile.php?id=100045360666811</a>
                </p>
            </div>
        </div>

    </div>
</template>

<script>

</script>

<style lang="scss" scoped>
.container {
    -moz-column-count: 2;
    -moz-column-gap: 20px;
    -moz-column-width: 50%;
    -webkit-column-count: 2;
    -webkit-column-gap: 20px;
    -webkit-column-width: 50%;
    column-count: 2;
    column-gap: 20px;
    column-width: 50%;

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

.container>* {
    margin-bottom: 50px;
    display: inline-block;
}



.member {
    width: 100%;

    img {
        width: 100%;
        height: 300px;
        object-fit: cover;
        object-position: center 20%;

        &:hover {
            transform: scale(1.05);
        }
    }

    .info {
        width: 100%;

        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: repeat(2, 1fr);
        grid-template-areas:
            "a b b"
            "a b b"
            "c c c";

        justify-items: start;
        align-items: center;

        h2 {
            grid-area: a;

            padding-top: 0;
            font-size: 110px;
            margin: 0;
            padding: 0;
        }

        h3 {
            grid-area: b;

            font-size: 25px;

            width: 100%;
        }

        p {
            grid-area: c;
        }
    }
}

@media screen and (max-width: 850px) {
    .container {
        display: flex;
        flex-direction: column;
        gap: 20px;

        h1 {
            font-size: 60px;
        }
    }

    img {
        pointer-events: none;
    }
}
</style>