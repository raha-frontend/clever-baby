<script setup lang="ts">
  import TheHeader from './components/TheHeader.vue';
  import HomeIntro from './components/HomeIntro.vue';
  import HomeStudy from './components/HomeStudy.vue';
</script>

<template>
  <div class="wrapper">
    <the-header />
    <home-intro />
    <home-study />

    <!-- <the-footer /> -->
  </div>
</template>

<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    margin: 0;
    font-family: "Roboto", sans-serif;
    color: var(--text-color);
  }

  :root {
    --text-color: #122659;
    --color-red: #ed1c21;
    --bg-color-btn: #FFD787;
    --bg-color-btn-sec: #8DD9E5;
    --bg-color-btn-ter: #FEB9CC;
    --color-black: #231f1e;
    --color-white: #fff;
  }

  a {
    text-decoration: none;
    color: var(--link-color);
  }

  ul {
    padding: 0;
    list-style: none;
  }

  .container {
    max-width: 930px;
    margin-right: auto;
    margin-left: auto;
  }

  .title {
    color: var(--text-color);
    font-size: 36px;
    font-style: normal;
    font-weight: 500;
    line-height: 140%;
  }
</style>
