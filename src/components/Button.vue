<template>
  <button
    :class="['btn', buttonTypeClass, sizeClass, customClass]"
    :disabled="disabled"
    @click="handleClick"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    type: {
      type: String,
      default: 'button',
    },
    buttonType: {
      type: String,
      default: 'primary',
    },
    size: {
      type: String,
      default: '',
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    customClass: {
      type: String,
      default: '',
    },
  },
  computed: {
    buttonTypeClass() {
      return `btn-${this.buttonType}`;
    },
    sizeClass() {
      return this.size ? `btn-${this.size}` : '';
    },
  },
  methods: {
    handleClick(event) {
      this.$emit('click', event);
    },
  },
};
</script>

<style scoped>
    .btn{
    background-color:$color-secondary ;
    }
</style>
