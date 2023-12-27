<template>
  <button :type="type" :class="{ btn: true, 'btn--outlined': outlined }">
    <!-- <button :type="type" :class="['btn', 'btn--outlined']"> -->
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "ButtonMain",
  props: {
    type: { type: String, default: "button" },
    outlined: {
      type: Boolean,
      default: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.btn {
  padding: 10px 20px;
  background: #ff6620;
  &--outlined {
    background: #ffffff;
    padding: 20px 40px;
  }
}
</style>
