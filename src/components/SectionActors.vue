<template lang="pug">
    section.section-actors
        div.container.container--section-actors
            div.section-actors--heading-wrapper
                h2.h2.h2--actors Актерский состав
                div.section-actors--slider-buttons
                    div.swiper-button-prev(slot="button-prev")
                    div.swiper-button-next(slot="button-next")
            div.swiper-pagination(slot="pagination")
        swiper
</template>

<script>
    import Swiper from "../components/Swiper";

    export default {
        name: "section-actors",
        data() {
            return {
            };
        },
        components: {
            Swiper,
        },
    };
</script>

<style lang="scss">
    @import "../assets/scss/general.scss";

    .container--section-actors {
        padding: 72px 120px 0;
    }

    .section-actors--heading-wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 24px;
    }

    .swiper-pagination {
        margin-bottom: 32px;
    }

    .section-actors--slider-buttons {
        display: flex;
        justify-content: right;
        gap: 40px;
    }

    div.swiper-button-prev, div.swiper-button-next {
        position: relative;
        background-size: 68%;
        margin-top: auto;

        &:hover {
            background-size: inherit;
        }
    }

    div.swiper-button-prev {
        background-image: url("../assets/arrow.svg");

        &:hover {
            background-image: url("../assets/arrow-hover.svg");
            transform: rotate(180deg);
        }
    }

    div.swiper-button-next {
        background-image: url("../assets/arrow.svg");
        transform: rotate(180deg);

        &:hover {
            background-image: url("../assets/arrow-hover.svg");
            transform: rotate(0);
        }
    }

    div.swiper-scrollbar {
        height: 2px;
        background: $redColor;
    }

    @media (max-width: 1024px) and (min-width: 768px) {

        .container--section-actors {
            padding: 65px 64px 0;
        }

        .section-actors--heading-wrapper {
            margin-bottom: 18px;
        }

        .swiper-pagination {
            margin-bottom: 25px;
        }

        .swiper-container {
            padding: 0 64px;
        }

        .swiper-slide {
            width: 40%;
        }

        .swiper__about-info {
            left: 17px;
            bottom: 70px;
        }

        .swiper__hero-description {
            bottom: 63px;
            left: 15px;
            max-width: 200px;
        }

        .swiper__hero, .swiper__name {
            font-size: 20px;
        }
    }

    @media (max-width: 767px) {

        .container--section-actors {
            padding: 13px 16px 0;
        }

        .swiper-container {
            width: 100%;
            padding: 0 16px;
        }

        .section-actors--heading-wrapper {
            margin-bottom: 17px;
        }

        .swiper-pagination {
            margin-bottom: 24px;
        }
    }

</style>