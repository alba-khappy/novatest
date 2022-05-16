<template lang="pug">
    section.section-logline
        div.container.container--section-logline
            h1.h1.h1--logline Сериал Ведьмак
            p.text-style--logline Геральт из Ривии, наемный охотник за&nbsp;чудовищами, перенесший мутации, идет навстречу своей судьбе в неспокойном мире, где люди часто оказываются куда коварнее чудовищ.
            a(href="").logline__btn Смотреть сериал
</template>

<script>
    export default {
        name: "section-logline",
        data() {
            return {
            };
        },
    };
</script>

<style lang="scss">
    @import "../assets/scss/general.scss";

    .section-logline {
        background: $blackColor url("../assets/section-logline-bg-1440.jpg") no-repeat center;
        background-size: cover;
    }

    .container--section-logline {
        color: $whiteColor;
        padding: 95px 120px 100px;
    }

    .h1--logline {
        margin-bottom: 18px;
    }

    .text-style--logline {
        max-width: 424px;
        margin-bottom: 40px;
        font-weight: 400;
        font-size: 16px;
    }

    .logline__btn {
        display: inline-block;
        background-color: $redColor;
        padding: 16px 46px;
        transition: background-color 0.3s;

        &:hover {
            background-color: $redColorHover;
        }
    }

    @media (max-width: 1024px) and (min-width: 768px) {

        .container--section-logline {
            padding: 54px 64px 78px;
        }

        .h1--logline {
            margin-bottom: 10px;
        }

        .text-style--logline {
            max-width: 345px;
            margin-bottom: 30px;
        }

        .section-logline {
            background-image: url("../assets/section-logline-bg-768.jpg");
        }
    }

    @media (max-width: 767px) {

        .h1--logline {
            margin-bottom: 3px;
        }

        .container--section-logline {
            padding: 53px 16px 73px;
        }

        .text-style--logline {
            max-width: 250px;
            margin-bottom: 30px;
        }

        .logline__btn {
            padding: 14px 37px;
        }

        .section-logline {
            background-image: url("../assets/section-logline-bg-360.jpg");
        }

        .section-actors--slider-buttons {
            gap: 20px;
        }

        div.swiper-button-prev, div.swiper-button-next {
            width: 28px;
            height: 28px;
        }

        .section-actors--heading-wrapper {
            margin-bottom: 17px;
        }

        .swiper-slide {
            width: 66%;
        }

        .swiper__link {
            height: 280px;
        }

        .swiper__about-info {
            left: 16px;
            bottom: 20px;
        }

        .swiper__hero, .swiper__name {
            font-size: 16px;
        }
    }

</style>