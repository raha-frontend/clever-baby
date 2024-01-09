<script lang="ts">
  import { defineComponent } from "vue";
  import AppButton from "./UI/AppButton.vue";

  export default defineComponent({
    name: "TheIntro",
    components: {AppButton},
  })
</script>

<template>
  <div class="intro">
    <div class="intro__inner container">
      <h1 class="intro__title title">Английский язык</h1>
      <span class="intro__age">для детей от 2 до 7 лет</span>
      <p class="intro__info">
        Гармоничное развитие детей и обучение <br>
        через полное погружение в языковую среду
      </p>
      <app-button class="app-btn">Записаться</app-button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .intro {
    min-width: 1366px;
    max-height: 512px;
    margin-right: auto;
    margin-left: auto;
    background-image: url(../assets/images/main-photo.jpg);
    background-repeat: no-repeat;
    background-size: cover;

    &__inner {
      position: relative;
      padding: 136px 0 160px 0;

      &::before {
        content: "";
        position: absolute;
        width: 106px;
        height: 84px;
        top: 37px;
        left: -153px;
        background-image: url(../assets/icons/car.svg);
        background-repeat: no-repeat;
      }

      &::after {
        content: "";
        position: absolute;
        width: 91px;
        height: 62px;
        top: 65px;
        right: -180px;
        background-image: url(../assets/icons/cloud.svg);
        background-repeat: no-repeat;
      }
    }

    &__title {
      margin-bottom: 15px;
      font-size: 42px;
    }

    &__age {
      display: block;
      margin-bottom: 30px;
      font-size: 18px;
      font-style: normal;
      font-weight: 500;
      line-height: 140%;
    }

    &__info {
      margin-bottom: 45px;
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 140%;
    }
  }
</style>