<template>
  <div class="teacher-card">
    <img
      :src="image"
      class="teacher-card__image"
      alt="teacher-img"
    />
    <span class="teacher-card__name">{{ name }}</span>
    <span class="teacher-card__country">{{ country }}</span>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TeacherCard",

  props: {
    image: {
      type: String,
      default: ''
    },
    name: {
      type: String,
      default: ''
    },
    country: {
      type: String,
      default: ''
    }
  }
})
</script>

<style lang="scss" scoped>
.teacher-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-width: 220px;

  &__image {
    display: block;
    margin-bottom: 20px;
    border-radius: 12px;
  }

  &__name {
    margin-bottom: 15px;
    font-size: 20px;
    font-weight: 500;
    line-height: 1;
  }

  &__country {
    font-size: 16px;
    font-weight: 400;
    line-height: 1;
    color: var(--country-text-color);
  }
}
</style>