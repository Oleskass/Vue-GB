<template>
  <div>
    <h1>
      {{ product.name }}
    </h1>
    <p>{{ formattedPrice }}</p>
    <p v-if="product.isAvailable">Product is available</p>
    <p v-else>Product is out of stock</p>
  </div>
</template>

<script>
export default {
  props: {
    product: Object,
  },

  computed: {
    formattedPrice() {
      return `$${this.product.price}`;
    },
  },
};
</script>

<style lang="scss" scoped>
div {
  border: 1px solid grey;
  width: 350px;
  margin-bottom: 10px;
}
</style>
