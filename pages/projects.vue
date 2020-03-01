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
            <carousel :items="items" :active="showProjects"/>
            <button class="carousel-button" :class="{'carousel-button-active' : showProjects}" v-on:click="showProjects = !showProjects"></button>
        </div>
    </div>
</template>

<script>
    import carousel from '~/components/carousel.vue'

    export default {
        components: {
            carousel
        },
        data(){
            return{
                showProjects: false,
                items: [
                    {
                        title: "Null Problems",
                        img: "logo-no-bg.png",
                        text: "Placeholder text because who doesn't need placeholder text"
                    },
                    {
                        title: "Test Title 2",
                        img: "placeholder.png",
                        text: "Placeholder text because who doesn't need placeholder text"
                    },
                    {
                        title: "Test Title 3",
                        img: "placeholder.png",
                        text: "Placeholder text because who doesn't need placeholder text"
                    },
                    {
                        title: "Test Title 4",
                        img: "placeholder.png",
                        text: "Placeholder text because who doesn't need placeholder text"
                    },
                    {
                        title: "Test Title 5",
                        img: "placeholder.png",
                        text: "Placeholder text because who doesn't need placeholder text"
                    }
                ],
            }
        }
    }
</script>

<style lang="scss">
    @import '~/styles/colors.scss';
    .carousel-button{
        position: absolute;
        z-index: 2;
        top: 50%;
        left: calc(100% - 64px);
        height: 64px;
        background: $primary;
        border: none;
        width: 64px;
        transform: translateY(-50%);
        transition: .5s;
        &.carousel-button-active{
            left: 0;
            transform: translateY(-50%) rotate(180deg);
        }
    }
    .color {
        color: $secondary;
    }

    .text {
        font-size: 16px;
        color: $primary;
    }
    .vertical{
        position: relative;
        flex: 1;
        height: 100%;
    }
</style>
