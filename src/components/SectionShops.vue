<template lang="pug">
    section.section-shops
        div.container.container--section-shops
            h2.h2.h2--shops Магазины мерча ведьмака
        div.container.container--map
            ShopOnTheMap(:coords="coords" :zoom="10" @click="onClick").ymaps-layers-pane
</template>

<script>

    import ShopOnTheMap from "../components/Map";

    export default {
        name: "section-shops",
        data() {
            return {
            };
        },
        components: {
            ShopOnTheMap,
            Map
        },
    };
</script>

<style lang="scss">
    @import "../assets/scss/general.scss";

    .map {
        width: 100%;
        height: 600px;
    }

    .container--section-shops {
        padding: 72px 120px 0;
    }

    .container--map {
        padding: 0 120px;
    }

    .h2--shops {
        margin-bottom: 40px;
    }

    .ymaps-layers-pane {
        filter: grayscale(1);
        -ms-filter: grayscale(1);
        -webkit-filter: grayscale(1);
        -moz-filter: grayscale(1);
        -o-filter: grayscale(1);
    }

    @media (max-width: 1024px) and (min-width: 768px){

        .container--section-shops {
            padding: 67px 64px 0;
        }

        .h2--shops {
            margin-bottom: 22px;
        }

        .container--map {
            padding: 0;
        }

        .ymap-container {
            height: 400px;
            margin-bottom: 0;
        }

    }

    @media (max-width: 767px) {

        .container--section-shops {
            padding: 16px;
        }

        .container--map {
            padding: 0;
        }

        .ymap-container {
            height: 400px;
            margin-bottom: 0;
        }

        .h2--shops {
            margin-bottom: 9px;
        }
    }

</style>