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

    return {
      nav,
    };
  },
});
</script>

<template>
  <header class="the-header">
    <div class="the-header__inner">
      <a class="the-header__logo" href="#">CleverBaby</a>

      <nav class="the-header__menu">
        <a
          v-for="(item, index) in nav"
          :key="index"
          href="#"
          class="the-header__menu-link"
        >
          {{ item.text }}
        </a>
      </nav>

      <a href="tel:+74959834719" class="the-header__tel">+ 7 (495) 983-47-19</a>
    </div>
  </header>
</template>

<style scoped lang="scss">
.the-header {
  padding: 30px 98px;

  &__inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1170px;
    margin-left: auto;
    margin-right: auto;
  }

  &__logo {
    display: block;
    margin-right: 47px;
    font-size: 23px;
    font-weight: 500;
  }

  &__menu {
    display: flex;
    align-items: center;
    margin-right: auto;
  }

  &__menu-link,
  &__tel {
    display: block;
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
