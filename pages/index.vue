<template>
    <div class="container">
        <div class="introduction">
            <h1 class="title">
                Tim Huijkman
            </h1>
            <h2 class="subtitle">
                Front-end Developer, Wanna be designer
            </h2>
            <nuxt-link to="contact">Contact me</nuxt-link>
        </div>
        <div class="logo">
            <logo/>
        </div>
    </div>
</template>

<script>
    import logo from '~/components/logo.vue'

    export default {
        components: {
            logo
        }
    }
</script>

<style lang="scss">
    @import '~/styles/colors.scss';

    .container {
        flex: 1;
        margin: 0 auto;
        min-height: 100vh;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .logo{
        height: 100%;
        flex: 1 0 40%;
    }

    .introduction{
        padding: 52px;
        flex: 0 0 60%;
        .title{
            color: $primary;
            font-size: 72px;
        }
        .subtitle{
            margin: 42px 0;
            font-weight: 200;
            color: $alternative;
            font-size: 42px;
        }
        a, button{
            display: block;
            width: max-content;
            min-width: 300px;
            margin: 64px 0;
            padding: 24px;
            border: solid 3px $secondary;
            color: $secondary;
            text-decoration: none;
            font-weight: 200;
            font-size: 32px;
        }
    }
</style>
