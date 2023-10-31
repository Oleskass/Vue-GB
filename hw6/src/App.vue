<template>
  <HeaderComponent />
  <IndexComponent />
  <BlogComponent />
  <ArticlesComponent />
  <ProjectComponent />
  <FooterComponent />
</template>

<script>
import IndexComponent from "./components/IndexComponent.vue";
import BlogComponent from "./components/BlogComponent.vue";
import ArticlesComponent from "./components/ArticlesComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
import ProjectComponent from "./components/ProjectComponent.vue";

export default {
  name: "App",
  components: {
    IndexComponent,
    BlogComponent,
    ArticlesComponent,
    HeaderComponent,
    FooterComponent,
    ProjectComponent,
  },
};
</script>

<style lang="scss"></style>
