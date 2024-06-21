<script setup>
const images = [
    "bmw-1",
    "img-2",
    "img-3",
    "img-4",
    "img-5",
    "img-6",
]
</script>

<template>
    <cardVue />
    <div class="main">
        <div class="main__info container">
            <h2 class="main__info-title">BMW</h2>
            <div class="main__info-galery">
                <div class="main__galery" v-for="(img, idx) of images" :key="idx">
                    <img :src="`/src/assets/img/${img}.png`" alt="" class="main__images-pic" />
                    <p class="main__info-text">Detail...</p>
                </div>
            </div>
            <div class="main__history">
                <div class="main__history-left">
                    <h2 class="main__history-title">
                        HISTORY
                    </h2>
                    <p class="main__history-text">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Arcu pretium proin rutrum nam sed nibh
                        condimentum id libero. Etiam non luctus scelerisque nec dignissim lobortis. Auctor feugiat
                        scelerisque eleifend arcu sed id donec dui eget. Elit elementum nam risus dignissim. Arcu fermentum
                        pharetra sed nunc.
                    </p>
                </div>
                <div class="main__history-img">
                    <img src="../assets/img/img-7.png" alt="">
                </div>
            </div>
            <div class="main__map">
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d4948724.774257701!2d5.174768300697382!3d51.056785865244926!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x479a721ec2b1be6b%3A0x75e85d6b8e91e55b!2z0JPQtdGA0LzQsNC90LjRjw!5e1!3m2!1sru!2s!4v1718994012502!5m2!1sru!2s"
                    width="1200" height="600" style="border:0;" allowfullscreen="" loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </div>
    </div>
    <footer class="footer">
        <h2 class="footer__title">
            ELITE
        </h2>
        <div class="footer__sciol">
            <img src="../assets/img/tg.png" alt="" class="footer__img">
            <img src="../assets/img/ins.png" alt="" class="footer__img">
            <img src="../assets/img/facebook.png" alt="" class="footer__img">
        </div>
        <div class="footer__number">
            +998 77 777 77 77
        </div>
    </footer>
</template>

<style lang="scss" scoped>
.main {
    background: #625451;
    padding: 30px 0;

    img {
        width: 370px;
        height: 300px;
    }

    &__info {
        &-title {
            text-align: center;
            font-weight: 500;
            font-size: 48px;
            color: #ffffff;
            margin-bottom: 40px;
        }
    }

    &__galery {
        width: 370px;
        position: relative;
    }

    &__info-galery {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        margin-bottom: 50px;
        row-gap: 20px;
    }

    &__info-text {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 24px;
        color: #fff;
        font-weight: 500;
        cursor: pointer;
        background: #00000040;
        backdrop-filter: blur(15px);
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        opacity: 0;
        transition: .3s;

        &:hover {
            opacity: 1;
        }
    }


    &__images-pic {
        width: 100%;
    }

    .main__history {
        display: flex;
        align-items: center;
        gap: 60px;
        justify-content: center;
        margin-bottom: 50px;
    }

    .main__history-title {
        font-size: 48px;
        font-weight: 500;
        text-align: center;
        color: #ffffff;
        margin-bottom: 30px;
    }

    .main__history-text {
        font-weight: 400;
        font-size: 24px;
        line-height: 30px;
        text-align: center;
        color: #ffffff;
        max-width: 653px;
    }
}

.footer {
    padding: 20px 0 32px 0;
    background: #313030;

    &__title {
        font-size: 30px;
        text-align: center;
        color: #ffffff;
        margin-bottom: 15px;
    }

    .footer__img {
        width: 40px;
        height: 40px;
    }

    .footer__sciol{
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 30px;
        margin-bottom: 15px;
        cursor: pointer;
    }

    .footer__number{
        text-align: center;
        color: #ffffff;
        font-size: 20px;
    }
}
</style>