<template>
  <div class="container">
    <slot>Defauly value</slot>
  </div>
</template>

<script>
export default {
  name: "ContainerMain",
};
</script>

<style lang="scss" scoped>
.container {
  max-width: 1110px;
  margin: 0 auto;
}
</style>
