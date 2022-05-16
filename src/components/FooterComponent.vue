<template lang="pug">
    footer.footer
        div.container.container--footer
            a(href="/").link-logo.footer__logo
            a(href="").link-privacy-policy Политика обработки персональных данных
            div.socials-links__container
                a(href="").socials-link.socials-link--inst
                a(href="").socials-link.socials-link--fb
                a(href="").socials-link.socials-link--vk
</template>

<script>

    export default {
        name: "footer-component",
        data() {
            return {
            };
        },
    };
</script>

<style lang="scss">
    @import "../assets/scss/general.scss";

    .footer {
        background: #343338;
    }

    .container--footer {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        padding: 42px 120px;
    }

    .socials-links__container {
        display: flex;
        justify-content: right;
        align-items: center;
        gap: 20px;
    }

    .link-privacy-policy {
        max-width: 170px;
        text-align: center;
        align-self: center;
        justify-self: center;
        font-weight: 400;
        font-size: 14px;
        text-decoration: underline;
        opacity: 0.7;
        transition: opacity 0.3s;

        &:hover {
            opacity: 1;
            text-decoration-color: #C2C1C3;
        }
    }

    .socials-link {
        width: 32px;
        height: 32px;
        transition: background 0.3s;
    }

    .socials-link--inst {
        background: transparent url("../assets/inst.svg") no-repeat center;
        &:hover {
            background-image: url("../assets/inst-hover.svg");
        }
    }

    .socials-link--fb {
        background: transparent url("../assets/facebook.svg") no-repeat center;
        &:hover {
            background-image: url("../assets/facebook-hover.svg");
        }
    }

    .socials-link--vk {
        background: transparent url("../assets/vk.svg") no-repeat center;

        &:hover {
            background-image: url("../assets/vk-hover.svg");
        }
    }

    @media (max-width: 1024px) and (min-width: 768px){

        .container--footer {
            padding: 42px 64px;
        }
    }

    @media (max-width: 767px) {

        .container--footer {
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, auto);
            padding: 28px 16px;
            gap: 28px 0;
        }

        a.footer__logo {
            width: 128px;
            height: 44px;
        }

        .socials-links__container {
            gap: 12px;
        }

        .link-privacy-policy {
            grid-area: 2/1/3/3;
            max-width: 300px;
            justify-self: left;
            text-align: left;
            opacity: 0.4;
        }

    }

</style>