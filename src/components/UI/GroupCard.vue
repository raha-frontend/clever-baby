<script lang="ts">
  import { defineComponent } from "vue";
  import AppButton from "./AppButton.vue";

  export default defineComponent({
    name: 'GroupCard',
    components: {AppButton},

    props: {
      title: {
        type: String,
        default: ''
      },

      week: {
        type: String,
        default: ''
      },

      hour: {
        type: String,
        default: ''
      },

      price: {
        type: Number,
        default: 0
      },

      color: {
        type: String,
        default: ''
      }
    }
  })
</script>

<template>
  <div class="card" :style="{'border-color': `var(${color})`}">
    <h4 class="card__title"> {{ title }} </h4>
    <span class="card__week"> {{ week }} </span>
    <span class="card__hour"> {{ hour }} </span>
    <div class="card__price"><span class="card__price-span"> {{ price }} &#8381;</span> в месяц</div>
    <app-button class="app-button_secondary" :color="color">Записаться</app-button>
  </div>
</template>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 50px 65px;
  border: 3px solid var(--bg-color-btn-sec);
  border-radius: 12px;

  &__title {
    margin-bottom: 40px;
    font-size: 20px;
    font-weight: 500;
    line-height: 1;
  }

  &__week,
  &__hour {
    margin-bottom: 20px;
    font-size: 16px;
    font-weight: 400;
    line-height: 1;
  }

  &__price {
    margin-bottom: 40px;
    font-size: 16px;
    font-weight: 400;
    line-height: 1;

    &-span {
      font-size: 20px;
      font-weight: 500;
      line-height: 1;
    }
  }
}
</style>
