<script lang="ts">
  import {defineComponent} from 'vue'

  export default defineComponent({
    props: {
      theme: {
        type: String,
        default: 'primary' // primary, secondory, tertiary
      },
      type: {
        type: String,
        default: 'button'
      },
      disabled: {
        type: Boolean,
        default: false
      }
    },

    setup() {

    }
  })
</script>

<template>
  <button
    :type="type"
    :disabled="disabled"
    :class="{ 'app-button_secondory': theme === 'secondory' }"
    class="app-btn"
  >
    <slot/>
  </button>
</template>

<style lang="scss" scoped>
  .app-btn {
    padding: 13px 31px 15px;
    font-size: 16px;
    background-color: var(--bg-color-btn);
    color: var(--text-color);
    border: none;
    border-radius: 35px;
    cursor: pointer;

    &:hover {
      background-color: var(--color-black);
      color: var(--color-white);
      transition: all 0.3s linear;
    }

    &_secondory {
      background-color: var(--bg-color-btn-sec);
    }
  }
</style>