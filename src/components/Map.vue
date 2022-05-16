<template lang="pug">
    div.ymap-container
        yandex-map(:coords="coords" :zoom="10" @click="onClick")
            ymap-marker (marker-id="123" :coords="coords" :icon="markerIcon")

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
                content: '123 v12',
                contentOffset: [0, 15],
                contentLayout: '<div style="background: red; width: 50px; color: #FFFFFF; font-weight: bold;"> Marker</div>'
            }
        })
    }

</script>

<style>
    .ymap-container {
        height: 540px;
        margin-bottom: 96px;
    }

</style>