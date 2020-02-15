<template>
    <div class="letterholder">
        <div class="letter">t</div>
    </div>
</template>

<style lang="scss">
    @import '~/styles/colors.scss';
    .letterholder{
        position: relative;
        width: 100%;
        height: 100%;
        overflow: hidden;
        padding: 5vw;
    }
    .letter{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%) scale(.8);
        font-size: 75vw;
        -webkit-background-clip: text;
        -webkit-text-stroke: 3px $complimentary;
        -webkit-text-fill-color: transparentize($alternative, .95);
        text-shadow: 0 0 $background, .70vw -.70vw  $secondary, -.35vw .35vw $complimentary;
    }
</style>