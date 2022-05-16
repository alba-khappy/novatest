<template lang="pug">
    div.ymap-container
        yandex-map(:coords="coords" :zoom="10" @click="onClick")
            ymap-marker(v-for="n in markers"
                :key="n.id"
                :marker-id="n.id"
                marker-type="placemark"
                :coords="n.coord"
                :balloon="{ body: n.text }")

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
            markers: [
                { coord: [55.7, 37.61] },
                { coord: [55.7, 37.65] },
                { coord: [55.7, 37.67] },
            ].map((n, i) => ({ ...n, id: i + 1 })),
        }),
        computed: {
            balloonTemplate() {
                return `
        <div class="red">
      `
            }
        },
        methods: {
            onClick(m) {
                this.$refs.map.myMap.balloon.open(m.coord);
            },
        }
    }
</script>

<style>
    .ymap-container {
        height: 540px;
        margin-bottom: 96px;
    }

    .red {
        width: 30px;
        height: 30px;
        background-color: #FF1E1E;
    }

</style>