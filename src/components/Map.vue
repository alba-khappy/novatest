<template lang="pug">
    div.ymap-container
        yandex-map(:coords="coords" :zoom="10" @click="onClick")
        ymap-marker(
        :coords="coords"
        marker-id="123"
        hint-content="some hint"
        )
</template>


<script>
    import { yandexMap } from 'vue-yandex-maps';

    export default {
        name: "shop-on-the-map",
        components: { yandexMap },
        data: () => ({
            coords: [
                55.751427, 37.618877
            ],
        }),
        methods: {
            onClick(e) {
                this.coords = e.get('coords');
            },
        },
    };

</script>

<style>
    .ymap-container {
        height: 540px;
        margin-bottom: 96px;
    }

</style>