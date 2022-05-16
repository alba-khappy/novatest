<template lang="pug">
    li.footage__img-item(:class="'footage__img-item-'+ index")
</template>

<script>
    export default {
        name: "footage-img",
        props: {
            index: {
                type: String,
            },
        },
        data() {
            return {
            };
        },
    };
</script>

<style lang="scss">
    @import "../assets/scss/general.scss";

    .footage__img-item {
        width: 100%;
        height: 100%;

        &:first-child {
            grid-area: 1/1/3/3;
        }
    }

    .footage__img-item-1 {
        background: transparent url("../assets/section-footage-1.jpg") no-repeat center;
    }

    .footage__img-item-2 {
        background: transparent url("../assets/section-footage-2.jpg") no-repeat center;
    }

    .footage__img-item-3 {
        background: transparent url("../assets/section-footage-3.jpg") no-repeat center;
    }

    .footage__img-item-4 {
        background: transparent url("../assets/section-footage-4.jpg") no-repeat center;
    }

    .footage__img-item-5 {
        background: transparent url("../assets/section-footage-5.jpg") no-repeat center;
    }

    @media (max-width: 1024px) and (min-width: 768px) {
        .footage__img-item {
            background-size: cover;
        }
    }

    @media (max-width: 767px) {
        .footage__img-item {
                height: 212px;
                background-size: cover;
                background-position-y: inherit;

            &:first-child {
                grid-area: 1/1/2/2;
            }
        }

        .footage__img-item-4, .footage__img-item-5 {
            display: none;
        }
    }



</style>