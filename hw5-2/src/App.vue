<template>
  <ProductListComponent />
</template>

<script>
import ProductListComponent from "./components/ProductListComponent.vue";

export default {
  components: { ProductListComponent },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
