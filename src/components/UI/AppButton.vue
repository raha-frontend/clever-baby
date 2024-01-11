<script lang="ts">
  import {defineComponent, computed} from 'vue'

  export default defineComponent({
    props: {
      theme: {
        type: String,
        default: 'primary' // primary, secondary, tertiary
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

    setup(props) {
      const classes = computed(() => ({
        'app-button_secondary': props.theme === 'secondary',
        'app-button_tertiary': props.theme === 'tertiary',
        'app-button_disabled' : props.disabled
      }))

      return {
        classes,
      }
    }
  })
</script>

<template>
  <button
    :type="type"
    :disabled="disabled"
    class="app-button"
    :class="classes"
  >
    <slot/>
  </button>
</template>

<style lang="scss" scoped>
  .app-button {
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

    &_secondary {
      background-color: var(--bg-color-btn-sec);
    }

    &_tertiary {
      background-color: var(--bg-color-btn-ter);
    }

    &_disabled {
      cursor: not-allowed;
      opacity: 0.8;

      &:hover {
        background-color: var(--bg-color-btn);
        color: var(--text-color);
      }
    }
  }
</style>