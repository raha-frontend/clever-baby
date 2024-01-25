<script lang="ts">
import { defineComponent, ref } from "vue";
import TeacherCard from "./UI/TeacherCard.vue";

interface TechCard {
  id: number;
  image: string;
  name: string;
  country: string;
}

export default defineComponent({
  name: "HomeTeacher",

  components: {
    TeacherCard
  },

  setup() {
    const TeacherCard = ref<TechCard[]>(
        [
          {
            id: 1,
            image: '../../public/images/kate.png',
            name: 'Kate Smith',
            country: 'США',
          },
          {
            id: 2,
            image: '../../public/images/samuel.png',
            name: 'Samuel King',
            country: 'США',
          },
          {
            id: 3,
            image: '../../public/images/nikole.png',
            name: 'Nikole Young',
            country: 'Канада',
          },
          {
            id: 4,
            image: '../../public/images/karoline.png',
            name: 'Karoline Bush',
            country: 'Канада',
          },
        ]
    );
    return {
      TeacherCard
    }
  }
})
</script>

<template>
  <div class="teachers">
    <div class="teachers__inner container">
      <div class="teachers__top">
        <h2 class="teachers__title">Наши преподаватели</h2>
        <div class="teachers__text">Все наши преподаватели — носители английского языка и имеют необходимое образование и опыт работы с детьми</div>
      </div>
      <div class="teachers__slider">
        <teacher-card
            v-for="card in TeacherCard"
            :key="card.id"
            :image="card.image"
            :name="card.name"
            :country="card.country"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.teachers {
  min-height: 714px;

  &__inner {
    padding: 130px 0;
  }

  &__top {
    position: relative;
    display: flex;
    justify-content: space-between;
    margin-bottom: 57px;

    &::after {
      content: "";
      position: absolute;
      width: 58px;
      height: 97px;
      top: -10px;
      right: -100px;
      background-image: url(../assets/icons/house.svg);
      background-repeat: no-repeat;
    }
  }

  &__title {
    font-size: 36px;
    font-weight: 500;
    line-height: 1;
  }

  &__text {
    max-width: 320px;
    margin-left: auto;
    font-size: 16px;
    font-weight: 400;
    line-height: 1.4;
  }

  &__slider {
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
    min-height: 340px;

    &::before {
      content: "";
      position: absolute;
      width: 44px;
      height: 132px;
      bottom: -2px;
      left: -146px;
      background-image: url(../assets/icons/pencil.svg);
      background-repeat: no-repeat;
    }
  }
}
</style>