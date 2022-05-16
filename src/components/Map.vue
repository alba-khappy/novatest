<template lang="pug">
    div.ymap-container
        yandex-map(:coords="coords" :zoom="10" @click="onClick")
            ymap-marker(marker-id="123" :coords="coords" :icon="markerIcon")
</template>


<script>
    import { yandexMap, ymapMarker } from 'vue-yandex-maps';

    export default {
        name: "shop-on-the-map",
        components: {yandexMap, ymapMarker},
        data: () => ({
            coords: [
                55.751427, 37.618877
            ],
            markerIcon: {
                layout: 'default#imageWithContent',
                imageHref: 'https://image.flaticon.com/icons/png/512/33/33447.png',
                imageSize: [43, 43],
                imageOffset: [0, 0],
                contentOffset: [0, 15],
                contentLayout: '<div style="width: 50px; color: #FFFFFF; font-weight: bold;"> <img src="../assets/mark.svg"> </div>'
            }
        }),
        methods: {
            onClick(e) {
                this.coords = e.get('coords');
            },
        },
    }
</script>

<style>
    .ymap-container {
        height: 540px;
        margin-bottom: 96px;
    }

</style>