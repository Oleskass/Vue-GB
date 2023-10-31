<template>
  <ItemComponent v-for="item in items" :key="item.id" :item="item" />
</template>

<script>
import ItemComponent from "./ItemComponent.vue";

export default {
  data() {
    return {
      items: [
        {
          id: 1,
          image: require("../assets/img/project_item1.png"),
          heading: "Minimal Bedroom",
          descr: "Decor / Artchitecture",
        },
        {
          id: 2,
          image: require("../assets/img/project_item2.png"),
          heading: "Minimal Bedroom",
          descr: "Decor / Artchitecture",
        },
        {
          id: 3,
          image: require("../assets/img/project_item3.png"),
          heading: "Classic Minimal Bedroom",
          descr: "Decor / Artchitecture",
        },
        {
          id: 4,
          image: require("../assets/img/project_item4.png"),
          heading: "Modern Bedroom",
          descr: "Decor / Artchitecture",
        },
        {
          id: 5,
          image: require("../assets/img/project_item5.png"),
          heading: "Minimal Bedroom table",
          descr: "Decor / Artchitecture",
        },
        {
          id: 6,
          image: require("../assets/img/project_item6.png"),
          heading: "System Table",
          descr: "Decor / Artchitecture",
        },
        {
          id: 7,
          image: require("../assets/img/project_item7.png"),
          heading: "Modern Bedroom",
          descr: "Decor / Artchitecture",
        },
        {
          id: 8,
          image: require("../assets/img/project_item8.png"),
          heading: "Modern Bedroom",
          descr: "Decor / Artchitecture",
        },
      ],
    };
  },
  components: { ItemComponent },
};
</script>

<style lang="scss" scoped></style>
