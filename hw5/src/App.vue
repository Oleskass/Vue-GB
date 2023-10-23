<template>
  <HeaderComponent />
  <IndexComponent />
  <BlogComponent />
  <ArticlesComponent />
  <FooterComponent />
</template>

<script>
import IndexComponent from "./components/IndexComponent.vue";
import BlogComponent from "./components/BlogComponent.vue";
import ArticlesComponent from "./components/ArticlesComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";

export default {
  // name: "App",
  components: {
    IndexComponent,
    BlogComponent,
    ArticlesComponent,
    HeaderComponent,
    FooterComponent,
  },
};
</script>

<style lang="scss"></style>
