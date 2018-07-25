<template>
  <button class="button-styles" :class="{'large': large}" @click="onClick">
    <slot></slot>
  </button>
</template>

<script>
  export default {
    name: 'my-button',

    props: {
      large: {
        type: Boolean,
        default: false
      }
    },

    methods: {
      onClick () {
        this.$emit('click');
      }
    }
  }
</script>

<style lang="scss">
  .button-styles {
    border: 1px solid #eee;
    border-radius: 3px;
    background-color: #FFFFFF;
    cursor: pointer;
    font-size: 15pt;
    padding: 3px 10px;
    margin: 10px;

    &.large {
      padding: 6px 14px;
    }
  }
</style>
