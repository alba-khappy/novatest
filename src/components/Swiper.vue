<template>
    <swiper :options="swiperOptions">
        <swiper-slide>
            <img src="../assets/section-actors-1.jpg">
        </swiper-slide>
        <swiper-slide>
            <img src="../assets/section-actors-2.jpg">
        </swiper-slide>
        <swiper-slide>
            <img src="../assets/section-actors-3.jpg">
        </swiper-slide>
        <swiper-slide>
            <img src="../assets/section-actors-4.jpg">
        </swiper-slide>
        <swiper-slide>
            <img src="../assets/section-actors-1.jpg">
        </swiper-slide>
        <swiper-slide>
            <img src="../assets/section-actors-2.jpg">
        </swiper-slide>
        <swiper-slide>
            <img src="../assets/section-actors-3.jpg">
        </swiper-slide>
        <swiper-slide>
            <img src="../assets/section-actors-4.jpg">
        </swiper-slide>

    </swiper>
</template>

<script>
    import 'swiper/dist/css/swiper.css'
    import { swiper, swiperSlide } from 'vue-awesome-swiper'

    export default {
        name: 'Swiper',
        components: {
            swiper,
            swiperSlide
        },
        data() {
            return {
                swiperOptions : {
                    slidesPerView: 5,
                    spaceBetween: 24,
                    freeMode: true,
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    }
                }
            }
        }
    }

</script>


<style scoped>
    .swiper-slide{
        display: flex;
        justify-content: center;
        flex-direction: column;
    }
    .swiper-container {
        height : 450px;
        width : 100%;
    }

</style>
