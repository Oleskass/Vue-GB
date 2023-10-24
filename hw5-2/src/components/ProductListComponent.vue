<template>
  <div>
    <ProductDetailsComponent
      v-for="product in products"
      :key="product.id"
      :product="product"
    />
  </div>
</template>

<script>
import ProductDetailsComponent from "./ProductDetailsComponent.vue";

export default {
  data() {
    return {
      products: [
        {
          id: 1,
          name: "Iron",
          price: 100,
          isAvailable: true,
        },
        {
          id: 2,
          name: "Kettle",
          price: 190,
          isAvailable: false,
        },
        {
          id: 3,
          name: "TV",
          price: 850,
          isAvailable: true,
        },
        {
          id: 4,
          name: "Vacuum cleaner",
          price: 220,
          isAvailable: true,
        },
        {
          id: 5,
          name: "Fan",
          price: 75,
          isAvailable: false,
        },
      ],
    };
  },

  components: { ProductDetailsComponent },
};
</script>

<style lang="scss" scoped></style>
