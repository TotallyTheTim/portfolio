<template>
    <div class="container">
        <div>
            <h1 class="title">
                Tim Huijkman
            </h1>
            <h2 class="subtitle">
                Front-end Developer, Wanna be designer
            </h2>
        </div>
    </div>
</template>

<script>
    // import circel from '~/components/circel.vue'

    export default {
        components: {
            // circel
        }
    }
</script>

<style lang="scss">
    @import '~/styles/colors.scss';

    .container {
        margin: 0 auto;
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .title {
        font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
        'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        display: block;
        font-weight: 300;
        font-size: 100px;
        color: $primary;
        letter-spacing: 1px;
    }

    .subtitle {
        font-weight: 300;
        font-size: 42px;
        color: $alternative;
        word-spacing: 5px;
        padding-bottom: 15px;
    }
</style>
