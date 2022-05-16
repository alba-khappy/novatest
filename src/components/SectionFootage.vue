<template lang="pug">
    section.section-footage
        div.container.container--section-footage
            h2.h2.h2--footage Кадры со съемок
            ul.footage__images-list
                footage-img(v-for="footageImage in footageImages",
                    :index="footageImage.index")
            button.footage__btn Показать еще
</template>

<script>
    import FootageImg from "../components/FootageImg";

    export default {
        name: "section-footage",
        data() {
            return {
                footageImages: [
                    {
                        index: "1",
                    },
                    {
                        index: "2",
                    },
                    {
                        index: "3",
                    },
                    {
                        index: "4",
                    },
                    {
                        index: "5",
                    },
                ],
            };
        },
        components: {
            FootageImg,
        },
    };
</script>

<style lang="scss">
    @import "../assets/scss/general.scss";

    .container--section-footage {
        padding: 68px 120px 0;
    }

    .h2--footage {
        margin-bottom: 40px;
    }

    .footage__images-list {
        display: grid;
        grid-template-rows: repeat(2, 1fr);
        grid-template-columns: repeat(4, 1fr);
        gap: 24px;
        height: 588px;
        margin-bottom: 32px;
    }

    .footage__btn {
        @include btnStyle;
        width: 100%;
        padding: 16px 0;
    }

    @media (max-width: 1024px) and (min-width: 768px) {

        .container--section-footage {
            padding: 25px 64px 0;
        }

        .h2--footage {
            margin-bottom: 21px;
        }

        .footage__images-list {
            height: 314px;
            margin-bottom: 26px;
        }
    }

    @media (max-width: 767px) {

        .container--section-footage {
            padding: 64px 16px 33px;
        }

        .h2--footage {
            margin-bottom: 24px;
        }

        .footage__images-list {
            grid-template-columns: 1fr;
            gap: 16px;
            height: auto;
            margin-bottom: 25px;
        }
    }

</style>