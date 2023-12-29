<template>
  <div class="wrapper-input">
    <!-- <input v-on="listeners" v-bind="$attrs" class="custom-input" /> -->
    <input type="text" v-bind="$attrs" class="custom-input" />
  </div>
</template>

<script>
export default {
  name: "CustomInput",
  //   computed: {
  //     listeners() {
  //       console.log(this.$attrs);
  //       return {
  //         ...this.$attrs,
  //         input: (event) => this.$emit("input", event.target.value),
  //       };
  //     },
  //   },
};
</script>

<style lang="scss" scoped>
@import "../../assets/scss/variables";

.wrapper-input {
  position: relative;
  display: inline-flex;
}

.custom-input {
  height: 40px;
  width: 100%;
  border: 2px solid $main-color;
  font-size: 18px;
  outline: none;
  line-height: inherit;
  padding: 8px 15px;

  &::placeholder {
    color: inherit;
  }

  &--error {
    border-color: red;
  }

  &__error {
    position: absolute;
    top: 100%;
    right: 0;
    width: 100%;
    font-size: 12px;
    color: red;
    line-height: 1.3;
  }
}
</style>
