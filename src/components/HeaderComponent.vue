<template lang="pug">
    header.header
        div.container.container--header
            a(href="/").link-logo
            a(href="").header__link.header__link--subscription Подключить подписку
</template>

<script>

    export default {
        name: "header-component",
        data() {
            return {
            };
        },
    };
</script>

<style lang="scss">
    @import "../assets/scss/general.scss";

    .container--header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 22px 120px;
    }

    .header__link--subscription {
        @include btnStyle;
        padding: 12px 27px;
    }

    @media (max-width: 1024px) and (min-width: 768px) {

        .container--header {
            padding: 13px 64px;
        }
    }

    @media (max-width: 767px) {

        .header__link--subscription {
            padding: 12px 20px;
        }

        .container--header {
            padding: 18px 16px;
        }
    }

</style>