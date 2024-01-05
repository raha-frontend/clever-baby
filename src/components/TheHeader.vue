<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TheHeader",

  setup() {
    const nav = [
      {
        text: "Методика",
      },
      {
        text: "Преподаватели",
      },
      {
        text: "Группы",
      },
      {
        text: "Отзывы",
      },
      {
        text: "Контакты",
      },
    ];
  },
});
</script>

<template>
  <header class="the-header">
    <div class="the-header__inner">
      <div class="the-header__left">
        <a class="the-header__logo" href="#">CleverBaby</a>

        <ul class="the-header__menu">
          <li class="the-header__item">
            <a href="#" class="the-header__menu-link">Методика</a>
          </li>
          <li class="the-header__item">
            <a href="#" class="the-header__menu-link">Преподаватели</a>
          </li>
          <li class="the-header__item">
            <a href="#" class="the-header__menu-link">Группы</a>
          </li>
          <li class="the-header__item">
            <a href="#" class="the-header__menu-link">Отзывы</a>
          </li>
          <li class="the-header__item">
            <a href="#" class="the-header__menu-link">Контакты</a>
          </li>
        </ul>
      </div>

      <div class="the-header__right">
        <a href="tel:+74959834719" class="the-header__tel"
          >+ 7 (495) 983-47-19</a
        >
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
.the-header {
  padding: 14px 98px;

  &__inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__left {
    display: flex;
    align-items: center;
  }

  &__logo {
    margin-right: 47px;
    font-size: 23px;
    font-weight: 500;
  }

  &__menu {
    display: flex;
    align-items: center;
  }

  &__menu-link,
  &__tel {
    padding: 10px;
    font-size: 16px;
    font-weight: 400;
    line-height: 140%;

    &:hover {
      color: var(--color-red);
      text-decoration: underline;
      transition: all 0.3s linear;
    }
  }

  &__tel {
    position: relative;
    font-size: 18px;

    &::before {
      content: "";
      position: absolute;
      width: 15px;
      height: 15px;
      top: 15px;
      left: -15px;
      background-image: url(../assets/icons/phone.svg);
      background-repeat: no-repeat;
    }
  }
}
</style>
