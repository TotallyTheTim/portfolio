<template>
    <div class="carousel">
        <template v-for="(item,index) in items">
            <div v-on:click="currentIndex = index"  class="item" :class="{
            'active': index === currentIndex,
            'next-active': index === currentIndex+1,
            'prev-active': index === currentIndex-1,
            'prev-far-active': index < currentIndex-1,
            'next-far-active': index > currentIndex+1
            }">
                <!--{{item.title}}-->
            </div>
        </template>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                items: [
                    {
                        title: "Test Title",
                        img: "placeholder.png",
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
                currentIndex: 1,
            }
        },
        methods:{
            setIndex(index){
                this.currentIndex = index;
            }
        }
    }
</script>

<style lang="scss">
    @import '~/styles/colors.scss';
    .carousel{
        width: calc(100% - 64px);
        height: 100%;
        position: relative;
        overflow: hidden;
        &:after, &:before{
        content: '';
            pointer-events: none;
            position: absolute;
            z-index: 1;
            width: 100%;
            height: 200px;
        }
        &:after{
            background-image: linear-gradient(180deg, transparent, $background 80%);
            bottom: 0;
        }
        &:before{
            background-image: linear-gradient(0deg, transparent, $background 80%);
            top: 0;
        }
        .item{
            width: 80%;
            position: absolute;
            left: 50%;
            height: calc(50% - 64px);
            background: $secondary;
            transition: top .3s ease-in-out;
            transform: translate(-50%, -50%);
            &.active{
                top: 50%;
            }
            &.prev-active{
                top: 0;
            }
            &.next-active{
                top: 100%;
            }
            &.next-far-active{
                top: 150%
            }
            &.prev-far-active{
                top: -50%
            }
        }
    }
</style>