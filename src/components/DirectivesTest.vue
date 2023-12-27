<template>
  <div v-if="isVisible">
    <h1>Directives 1</h1>
  </div>
  <div v-show="isVisible">
    <h1>Directives 2</h1>
  </div>
  <ul>
    <template v-for="fruit in fruits">
      <li v-if="fruit !== 'banana'" :key="fruit">{{ fruit }}</li>
    </template>
  </ul>
</template>

<script>
export default {
  name: "DirectivesTest",
  data() {
    return {
      isVisible: false,
      fruits: ["kivi", "mango", "banana"],
    };
  },
};
</script>

<style lang="scss" scoped></style>
