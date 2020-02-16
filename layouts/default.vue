<template>
  <div id="main">
    <nav>
      <nuxt-link to="/" class="nav-link">
        <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="home-lg" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" class="svg-inline--fa fa-home-lg fa-w-18 fa-3x"><path fill="" d="M570.69 236.28L512 184.45V48a16 16 0 0 0-16-16h-64a16 16 0 0 0-16 16v51.69L314.75 10.31a39.85 39.85 0 0 0-53.45 0l-256 226a16 16 0 0 0-1.21 22.6L25.5 282.7a16 16 0 0 0 22.6 1.21L277.42 81.63a16 16 0 0 1 21.17 0L527.91 283.9a16 16 0 0 0 22.6-1.21l21.4-23.82a16 16 0 0 0-1.22-22.59zM288 115L69.47 307.71c-1.62 1.46-3.69 2.14-5.47 3.35V496a16 16 0 0 0 16 16h128a16 16 0 0 0 16-16V368a16 16 0 0 1 16-16h96a16 16 0 0 1 16 16v128a16 16 0 0 0 16 16h128a16 16 0 0 0 16-16V311.1c-1.7-1.16-3.72-1.82-5.26-3.2z" class=""></path></svg>
      </nuxt-link>
      <nuxt-link to="about" class="nav-link">
        <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="user" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" class="svg-inline--fa fa-user fa-w-14 fa-3x"><path fill="" d="M224 256c70.7 0 128-57.3 128-128S294.7 0 224 0 96 57.3 96 128s57.3 128 128 128zm89.6 32h-16.7c-22.2 10.2-46.9 16-72.9 16s-50.6-5.8-72.9-16h-16.7C60.2 288 0 348.2 0 422.4V464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48v-41.6c0-74.2-60.2-134.4-134.4-134.4z" class=""></path></svg>
      </nuxt-link>
      <nuxt-link to="projects" class="nav-link">
        <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="eye" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" class="svg-inline--fa fa-eye fa-w-18 fa-3x"><path fill="" d="M572.52 241.4C518.29 135.59 410.93 64 288 64S57.68 135.64 3.48 241.41a32.35 32.35 0 0 0 0 29.19C57.71 376.41 165.07 448 288 448s230.32-71.64 284.52-177.41a32.35 32.35 0 0 0 0-29.19zM288 400a144 144 0 1 1 144-144 143.93 143.93 0 0 1-144 144zm0-240a95.31 95.31 0 0 0-25.31 3.79 47.85 47.85 0 0 1-66.9 66.9A95.78 95.78 0 1 0 288 160z" class=""></path></svg>
      </nuxt-link>
      <nuxt-link to="skills" class="nav-link">
        <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="stars" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="svg-inline--fa fa-stars fa-w-16 fa-3x"><path fill="" d="M259.69042,85.96457l49.64549,20.69969,20.70353,49.643a6.65746,6.65746,0,0,0,11.926,0L362.667,106.66426l49.64549-20.69969a6.66574,6.66574,0,0,0,0-11.92493L362.667,53.338,341.96545,3.697a6.65746,6.65746,0,0,0-11.926,0L309.33591,53.338,259.69042,74.03964a6.66574,6.66574,0,0,0,0,11.92493ZM364.294,267.29343,259.4951,251.99764l-46.90716-95.19633c-8.39078-16.99879-32.68813-17.2019-41.18829,0l-46.90716,95.19633L19.69358,267.29343C.89634,269.99636-6.71318,293.19783,6.99021,306.49376l75.90772,73.99472L64.89758,485.07476c-3.20319,18.9049,16.68782,33.107,33.29752,24.2014l93.7987-49.3871,93.79869,49.3871A22.95361,22.95361,0,0,0,319.09,485.07476L301.199,380.48848l75.89209-73.99472C390.70077,293.19783,383.09125,269.99636,364.294,267.29343ZM509.05268,219.2285,469.339,202.67109,452.7801,162.961a5.32691,5.32691,0,0,0-9.5412,0L426.678,202.67109l-39.7117,16.55741a5.33385,5.33385,0,0,0,0,9.54033L426.678,245.3282l16.56087,39.7081a5.32534,5.32534,0,0,0,9.5412,0L469.339,245.3282l39.71366-16.55937a5.33386,5.33386,0,0,0,0-9.54033Z" class=""></path></svg>
      </nuxt-link>
      <nuxt-link to="contact" class="nav-link">
        <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="envelope" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="svg-inline--fa fa-envelope fa-w-16 fa-3x"><path fill="" d="M502.3 190.8c3.9-3.1 9.7-.2 9.7 4.7V400c0 26.5-21.5 48-48 48H48c-26.5 0-48-21.5-48-48V195.6c0-5 5.7-7.8 9.7-4.7 22.4 17.4 52.1 39.5 154.1 113.6 21.1 15.4 56.7 47.8 92.2 47.6 35.7.3 72-32.8 92.3-47.6 102-74.1 131.6-96.3 154-113.7zM256 320c23.2.4 56.6-29.2 73.4-41.4 132.7-96.3 142.8-104.7 173.4-128.7 5.8-4.5 9.2-11.5 9.2-18.9v-19c0-26.5-21.5-48-48-48H48C21.5 64 0 85.5 0 112v19c0 7.4 3.4 14.3 9.2 18.9 30.6 23.9 40.7 32.4 173.4 128.7 16.8 12.2 50.2 41.8 73.4 41.4z" class=""></path></svg>
      </nuxt-link>
    </nav>
    <nuxt />
  </div>
</template>

<style lang="scss">
  @import '~/styles/colors.scss';
  @import url('https://fonts.googleapis.com/css?family=Roboto:300,400,500,700&display=swap');

  html {
    font-family: Roboto, sans-serif;
    font-size: 16px;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
    background: $background;
  }

  *,
  *:before,
  *:after {
    box-sizing: border-box;
    margin: 0;
  }
  #main{
    display: flex;
  }
  nav{
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    flex: 0 0 62px;
    background: transparentize(darken($alternative,15%), .25);
  }
  .nav-link{
    margin: 4px 0;
    padding: 4px;
    display: block;
    &.nuxt-link-exact-active svg path{
      fill: $secondary;
    }
    &:hover svg path{
      fill: desaturate($secondary,80%);
    }
    svg{
      width: 24px;
      height: 24px;
      path{
        fill: $alternative;

      }
    }
  }
</style>
