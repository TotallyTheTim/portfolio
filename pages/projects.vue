<template>
    <div class="container">
        <div class="introduction introduction-smaller" :class="{'pushed' : showProjects}">
            <h1 class="title">
                WORKS <span class="color">&</span> DEMO'S
            </h1>
            <div class="text">
                A couple of projects, works and demo's to show you, the user what I can do, and what I've done.
            </div>
        </div>
        <div class="vertical">
            <carousel :items="items" @setIndex="setIndex" :active="showProjects"/>
            <div class="carousal-info" :class="{'hidden' : !showProjects}">
                <div v-if="index !== null">
                    <transition name="fade">
                        <div v-if="index % 2 === 0">
                            <h1>{{items[index].title}}</h1>
                            <p v-html="items[index].text"></p>
                        </div>
                    </transition>
                    <transition name="fade">
                        <div v-if="index % 2 !== 0">
                            <h1>{{items[index].title}}</h1>
                            <p v-html="items[index].text"></p>
                        </div>
                    </transition>


                </div>
            </div>
            <button class="carousel-button" :class="{'carousel-button-active' : showProjects}"
                    v-on:click="showProjects = !showProjects"></button>
        </div>
    </div>
</template>

<script>
    import carousel from '~/components/carousel.vue'

    export default {
        components: {
            carousel
        },
        methods: {
            setIndex(i) {
                this.index = i;
            }
        },
        data() {
            return {
                showProjects: false,
                index: null,
                items: [
                    {
                        title: "Null Problems",
                        img: "logo-no-bg.png",
                        text: "Well hello there, as you can see you can put text here!, it's also possible to do some <b>bold</b> text or even some <i>italic</i>!"
                    },
                    {
                        title: "Test Title 2",
                        img: "placeholder.png",
                        text: "<p>You can also do multiple lines</p><p>It's truelly amazing isn't it?</p>"
                    },
                    {
                        title: "Test Title 3",
                        img: "logo-no-bg.png",
                        text: "Could probably insert some images aswell but I haven't worked out what's the best way to do that yet ☺"
                    },
                    {
                        title: "Test Title 4",
                        img: "placeholder.png",
                        text: "And yeah I hope you enjoy the look of this"
                    },
                    {
                        title: "Test Title 5",
                        img: "logo-no-bg.png",
                        text: "Placeholder text because who doesn't need placeholder text"
                    }
                ],
            }
        }
    }
</script>

<style lang="scss">
    @import '~/styles/colors.scss';

    .carousel-button {
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

        &.carousel-button-active {
            left: 0;
            transform: translateY(-50%) rotate(180deg);
        }
    }

    .color {
        color: $secondary;
    }

    .carousal-info {
        top: 0;
        right: 0;
        position: absolute;
        height: 100%;
        width: calc(50% - 32px);
        transition: right .3s ease-in-out;

        > div {
            position: relative;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;

            > div {
                width: 100%;
                position: absolute;
                color: $secondary;
            }
        }

        &.hidden {
            right: calc(-50% + 32px);
        }
    }

    .text {
        font-size: 16px;
        color: $primary;
    }

    .vertical {
        overflow: hidden;
        position: relative;
        flex: 1;
        height: 100%;
    }

    .introduction {
        transition: margin-left .3s ease-in-out;
    }

    .pushed {
        margin-left: -50%;
    }

    .fade-enter-active, .fade-leave-active {
        transition: .5s;
    }

    .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */
    {
        opacity: 0;
    }

    .fade-enter {
        transform: translate(12.5%) rotate(45deg) scale(.5);
        filter: blur(1px);
    }

    .fade-leave-to {
        transform: translate(50%) rotate(-15deg) scale(2);
        filter: blur(4px);
    }
</style>
