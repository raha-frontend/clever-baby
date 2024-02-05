<script lang="ts">
import {defineComponent, ref} from "vue";
import 'vue3-carousel/dist/carousel.css';
import {Carousel, Slide, Navigation} from 'vue3-carousel';

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
    TeacherCard,
    Carousel,
    Slide,
    Navigation,
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
        <div class="teachers__text">Все наши преподаватели — носители английского языка и имеют необходимое образование
          и опыт работы с детьми
        </div>
      </div>
      <div class="teachers__slider">
        <carousel :items-to-show="4">
          <slide
              v-for="card in TeacherCard"
              :key="card.id"
          >
            <teacher-card
                :image="card.image"
                :name="card.name"
                :country="card.country"
            />
          </slide>

          <template #addons>
            <navigation/>
          </template>
        </carousel>
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
    min-height: 340px;

    :deep(.carousel__viewport) {
      position: relative;
    }

    :deep(.carousel__track) {
      column-gap: 2px;
    }

    :deep(.carousel__prev) {
      left: 47%;
      background-image: url(../assets/icons/slide-left.svg);
    }

    :deep(.carousel__next) {
      right: 46%;
      background-image: url(../assets/icons/slide-right.svg);
    }

    :deep(.carousel__prev),
    :deep(.carousel__next){
      content: "";
      position: absolute;
      width: 17px;
      height: 10px;
      top: 340px;
      background-repeat: no-repeat;
      color: transparent;
    }

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