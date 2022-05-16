<template lang="pug">
    swiper(:options="swiperOptions")
        swiper-slide(v-for = "slide in slides")
            actor-component(
                :index = "slide.index",
                :hero = "slide.hero",
                :name = "slide.name",
                :descr = "slide.descr"
            )
</template>

<script>
    import 'swiper/dist/css/swiper.css'
    import { swiper, swiperSlide } from 'vue-awesome-swiper'
    import ActorComponent from "./ActorComponent";

    export default {
        title: 'Progress pagination',
        name: 'Swiper',
        components: {
            ActorComponent,
            swiper,
            swiperSlide,
        },
        data() {
            return {
                swiperOptions : {
                    slidesPerView: 'auto',
                    spaceBetween: 24,
                    freeMode: true,
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    },
                    pagination: {
                            el: '.swiper-pagination',
                            type: 'progressbar'
                        },
                },
                slides: [
                    {
                        index: 1,
                        hero: "Геральт",
                        name: "Генри Кавилл",
                        descr: "Один из центральных персонажей сериала, лучший друг и неизменный спутник Геральта, трубадур и бабник"
                    },
                    {
                        index: 2,
                        hero: "Лютик",
                        name: "Джои Бэти",
                        descr: "Один из центральных персонажей сериала, лучший друг и неизменный спутник Геральта, трубадур и бабник"
                    },
                    {
                        index: 3,
                        hero: "Йеннифэр",
                        name: "Аня Чалотра",
                        descr: "Один из центральных персонажей сериала, лучший друг и неизменный спутник Геральта, трубадур и бабник"
                    },
                    {
                        index: 4,
                        hero: "Цири",
                        name: "Фрейя Аллан",
                        descr: "Один из центральных персонажей сериала, лучший друг и неизменный спутник Геральта, трубадур и бабник"
                    },
                    {
                        index: 5,
                        hero: "Эмгыр вар Эмрейс",
                        name: "Барт Эдвардс",
                        descr: "Один из центральных персонажей сериала, лучший друг и неизменный спутник Геральта, трубадур и бабник"
                    },
                    {
                        index: 6,
                        hero: "Геральт",
                        name: "Генри Кавилл",
                        descr: "Один из центральных персонажей сериала, лучший друг и неизменный спутник Геральта, трубадур и бабник"
                    },

                ],
            }
        }
    }

</script>


<style lang="scss">
    @import "../assets/scss/general.scss";

    .swiper-slide{
        display: flex;
        justify-content: center;
        flex-direction: column;
        width: 23%;
    }
    .swiper-container {
        width: 100%;
        padding: 0 120px;
    }

    .swiper-pagination-progressbar {
        position: relative;
        height: 2px;
        width: 100%;
        background-color: #5D5D5D;
    }

    .swiper-pagination-progressbar .swiper-pagination-progressbar-fill {
        background-color: $redColor;
    }

    @media (max-width: 1024px) and (min-width: 768px){

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

        .swiper-container {
            width: 100%;
            padding: 0 16px;
        }

        .section-actors--slider-buttons {
            gap: 20px;
        }

        div.swiper-button-prev, div.swiper-button-next {
            width: 28px;
            height: 28px;
        }

        .swiper-pagination {
            margin-bottom: 24px;
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

        .swiper-pagination {
            margin-bottom: 24px;
        }
    }


</style>
