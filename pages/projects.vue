<template>
    <div class="container">
        <div class="introduction introduction-smaller">
            <h1 class="title">
                WORKS <span class="color">&</span> DEMO'S
            </h1>
            <div class="text">
                A couple of projects, works and demo's to show you, the user what I can do, and what I've done.
            </div>
        </div>
        <div class="vertical">
            <carousel/>
        </div>
    </div>
</template>

<script>
    import carousel from '~/components/carousel.vue'

    export default {
        components: {
            carousel
        }
    }
</script>

<style lang="scss">
    @import '~/styles/colors.scss';

    .color {
        color: $secondary;
    }

    .text {
        font-size: 16px;
        color: $primary;
    }
    .vertical{
        flex: 1;
        height: 100%;
    }
</style>
