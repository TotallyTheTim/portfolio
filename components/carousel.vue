<template>
    <div class="carousel" :class="{'alternative-position' : active}">
        <template v-for="(item,index) in items">
            <div @click="setIndex(index)" class="item" :class="{
            'active': index === currentIndex,
            'next-active': index === currentIndex+1,
            'prev-active': index === currentIndex-1,
            'prev-far-active': index < currentIndex-1,
            'next-far-active': index > currentIndex+1
            }">
                <div class="item-inner">
                    <div class="item-background"
                         :style="{ backgroundImage: 'url(' + require(`@/assets/projects/${item.img}`) + ')' }"></div>
                </div>
            </div>
        </template>
    </div>
</template>

<script>
    export default {
        props: {
            items: {
                type: Array,
                required: true,
            },
            active: {
                type: Boolean,
                required: true,
            }
        },
        data() {
            return {
                currentIndex: 1,
            }
        },
        mounted() {
            this.updateParentIndex();
        },
        methods: {
            setIndex(index) {
                this.currentIndex = index;
                this.updateParentIndex();
            },
            updateParentIndex() {
                this.$emit('setIndex', this.currentIndex);
            },
            getUrl(url) {
                // return require('/assets/projects/${url}')
            }
        }
    }
</script>

<style lang="scss">
    @import '~/styles/colors.scss';

    .carousel {
        max-width: calc(100% - 64px);
        height: 100%;
        flex: 0 0 100%;
        position: relative;
        overflow: hidden;
        justify-self: flex-end;
        transition: max-width .3s ease-in-out, margin-left .3s ease-in-out, flex .3s ease-in-out;

        &.alternative-position {
            max-width: calc(50% - 32px);
            margin-left: 48px;
            flex: 0 0 50%;
        }

        &:after, &:before {
            content: '';
            pointer-events: none;
            position: absolute;
            z-index: 1;
            width: 100%;
            height: 200px;
        }

        &:after {
            background-image: linear-gradient(180deg, transparent, $background 80%);
            bottom: 0;
        }

        &:before {
            background-image: linear-gradient(0deg, transparent, $background 80%);
            top: 0;
        }

        .item {
            width: 80%;
            position: absolute;
            left: 50%;
            height: calc(50% - 64px);
            background: $secondary;
            transition: top .3s ease-in-out;
            transform: translate(-50%, -50%);

            &.active {
                top: 50%;
            }

            &.prev-active {
                top: 0;
            }

            &.next-active {
                top: 100%;
            }

            &.next-far-active {
                top: 150%
            }

            &.prev-far-active {
                top: -50%
            }
        }

        .item-inner {
            width: 100%;
            height: 100%;
            position: relative;
        }

        .item-background {
            background-size: cover;
            background-position: center;
            width: 100%;
            height: 100%;
            position: absolute;
        }
    }
</style>