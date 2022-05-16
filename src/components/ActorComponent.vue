<template lang="pug">
        a(href="").swiper__link(:class="'section-actors__img-'+ index")
            div.swiper__about-info
                p.swiper__hero {{hero}}
                p.swiper__name {{name}}
            p.swiper__hero-description {{descr}}
</template>

<script>
    export default {
        name: "actor-component",
        props: {
                index: {
                    type: Number,
                },
                hero: {
                    type: String,
                },
                name: {
                    type: String,
                },
                descr: {
                    type: String,
                }
        },
        data() {
            return {
            };
        },
    };
</script>

<style lang="scss">
    @import "../assets/scss/general.scss";

    .swiper__link {
        height: 400px;
        position: relative;
    }

    .swiper__about-info {
        position: absolute;
        left: 23px;
        bottom: 41px;
    }

    .swiper__hero {
        font-weight: 600;
        font-size: 24px;
    }

    .swiper__name {
        font-weight: 400;
        font-size: 24px;
    }

    .section-actors__img-1 {
        background: url("../assets/section-actors-1.jpg") no-repeat top;
        background-size: cover;

        &:hover {
            background: linear-gradient(0deg, rgba(24, 24, 24, 0.8), rgba(24, 24, 24, 0.8)), url("../assets/section-actors-1.jpg") no-repeat top;
            background-size: cover;
        }

        &:hover .swiper__about-info {
            top: 45px;
        }

        &:hover .swiper__hero-description {
            display: block;
        }
    }

    .swiper__hero-description {
        display: none;
        position: absolute;
        bottom: 45px;
        left: 20px;
        text-align: left;
        margin: 0 auto;
    }

    .section-actors__img-2 {
        background: url("../assets/section-actors-2.jpg") no-repeat top;
        background-size: cover;

        &:hover {
            background: linear-gradient(0deg, rgba(24, 24, 24, 0.8), rgba(24, 24, 24, 0.8)), url("../assets/section-actors-2.jpg") no-repeat top;
            background-size: cover;
        }

        &:hover .swiper__about-info {
            top: 20px;
        }

        &:hover .swiper__hero-description {
            display: block;
        }
    }

    .section-actors__img-3 {
        background: url("../assets/section-actors-3.jpg") no-repeat top;
        background-size: cover;

        &:hover {
            background: linear-gradient(0deg, rgba(24, 24, 24, 0.8), rgba(24, 24, 24, 0.8)), url("../assets/section-actors-3.jpg") no-repeat top;
            background-size: cover;
        }

        &:hover .swiper__about-info {
            top: 20px;
        }

        &:hover .swiper__hero-description {
            display: block;
        }
    }

    .section-actors__img-4 {
        background: url("../assets/section-actors-4.jpg") no-repeat top;
        background-size: cover;

        &:hover {
            background: linear-gradient(0deg, rgba(24, 24, 24, 0.8), rgba(24, 24, 24, 0.8)), url("../assets/section-actors-4.jpg") no-repeat top;
            background-size: cover;
        }

        &:hover .swiper__about-info {
            top: 20px;
        }

        &:hover .swiper__hero-description {
            display: block;
        }
    }

    .section-actors__img-5 {
        background: url("../assets/section-actors-1.jpg") no-repeat top;
        background-size: cover;

        &:hover {
            background: linear-gradient(0deg, rgba(24, 24, 24, 0.8), rgba(24, 24, 24, 0.8)), url("../assets/section-actors-1.jpg") no-repeat top;
            background-size: cover;
        }

        &:hover .swiper__about-info {
            top: 20px;
        }

        &:hover .swiper__hero-description {
            display: block;
        }
    }

    .section-actors__img-6 {
        background: url("../assets/section-actors-2.jpg") no-repeat top;
        background-size: cover;

        &:hover {
            background: linear-gradient(0deg, rgba(24, 24, 24, 0.8), rgba(24, 24, 24, 0.8)), url("../assets/section-actors-2.jpg") no-repeat top;
            background-size: cover;
        }

        &:hover .swiper__about-info {
            top: 20px;
        }

        &:hover .swiper__hero-description {
            display: block;
        }
    }

</style>