<script lang="ts">
  import { defineComponent, ref } from "vue";

  import AppButton from "./UI/AppButton.vue";
  import GroupCard from "./UI/GroupCard.vue";

  interface Card {
    id: number;
    title: string;
    week: string;
    hour: string;
    price: number;
    color: string;
  }

  export default defineComponent({
    name: "HomeGroups",

    components: {
      AppButton,
      GroupCard,
    },

    setup() {
      const cardList = ref<Card[]>(
          [
            {
              id: 1,
              title: 'Бэбики-1',
              week: '1 раз в неделю',
              hour: '1,5 часа занятие',
              price: 2500,
              color: '--bg-color-btn-sec'
            },
            {
              id: 2,
              title: 'Бэбики-2',
              week: '2 раз в неделю',
              hour: '1,5 часа занятие',
              price: 4000,
              color: '--bg-color-btn'
            },
            {
              id: 3,
              title: 'Бэбики-3',
              week: '3 раз в неделю',
              hour: '1 часа занятие',
              price: 4000,
              color: '--bg-color-btn-ter'
            },
          ]
      );

      return{
        cardList,
      }
    },
  })
</script>

<template>
  <div class="groups">
    <div class="groups__inner container">
      <div class="groups__top">
        <h2 class="groups__title">Наши группы</h2>
        <div class="groups__text">В группах занимается до 5 человек. Все дети в группе примерно одного возраста и уровня знаний.</div>
      </div>
      <div class="groups__card">
        <group-card
            v-for="card in cardList"
            :key="card.id"
            :title="card.title"
            :week="card.week"
            :hour="card.hour"
            :price="card.price"
            :color="card.color"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.groups {
  min-height: 803px;
  background-image: url(../assets/images/backgr-groups.png);
  background-repeat: no-repeat;
  background-position: center top;

  &__inner {
    padding: 183px 0;
  }

  &__top {
    display: flex;
    justify-content: space-between;
    margin-bottom: 57px;
  }

  &__title {
    position: relative;
    font-size: 36px;
    font-weight: 500;
    line-height: 1;

    &::before {
      content: "";
      position: absolute;
      width: 56px;
      height: 58px;
      top: -70px;
      left: -60px;
      background-image: url(../assets/icons/star.svg);
      background-repeat: no-repeat;
    }
  }

  &__text {
    max-width: 272px;
    margin-left: auto;
    font-size: 16px;
    font-weight: 400;
    line-height: 1.4;
  }

  &__card {
    display: flex;
    justify-content: space-between;
  }
}
</style>

