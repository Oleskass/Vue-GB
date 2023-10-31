<template>
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Project</title>
      <link rel="preconnect" href="https://fonts.googleapis.com" />
      <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
      <link
        href="https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=Jost:wght@400;600&display=swap"
        rel="stylesheet"
      />
      <link rel="stylesheet" href="style.css" />
    </head>
    <body>
      <div id="app">
        <section class="banner__project banner">
          <div class="banner__box">
            <h2 class="banner__heading">Our Project</h2>
            <div class="banner__nav">
              <a href="index.html">Home</a>
              /
              <a href="blog.html">Blog</a>
            </div>
          </div>
        </section>
        <div class="projects">
          <div class="categories center">
            <div class="categories__content">
              <button class="categories__btn">Bathroom</button>
              <button class="categories__btn">Bed Room</button>
              <button class="categories__btn">Kitchen</button>
              <button class="categories__btn">Living Area</button>
            </div>
          </div>
          <div class="item__component center">
            <ItemListComponent />
          </div>
          <div class="pagination center">
            <PaginationComponent />
          </div>
        </div>
      </div>
    </body>
  </html>
</template>

<script>
import ItemListComponent from "./ItemListComponent.vue";
import PaginationComponent from "./PaginationComponent.vue";

export default {
  data() {
    return {
      cards: [
        {
          img: require("../assets/img/blog_item_img1.png"),
          tag: "Kitchen Design",
          title: "Let’s Get Solution For Building Construction Work",
          date: "26 December, 2022 ",
        },
        {
          img: require("../assets/img/blog_item_img2.png"),
          tag: "Living Design",
          title: "Low Cost Latest Invented Interior Designing Ideas.",
          date: "22 December, 2022 ",
        },
        {
          img: require("../assets/img/blog_item_img3.png"),
          tag: "Interior Design",
          title: "Best For Any Office & Business Interior Solution",
          date: "25 December, 2022 ",
        },
        {
          img: require("../assets/img/blog_item_img4.png"),
          tag: "Kitchen Design",
          title: "Let’s Get Solution For Building Construction Work",
          date: "26 December, 2022 ",
        },
        {
          img: require("../assets/img/blog_item_img5.png"),
          tag: "Living Design",
          title: "Low Cost Latest Invented Interior Designing Ideas.",
          date: "22 December, 2022 ",
        },
        {
          img: require("../assets/img/blog_item_img6.png"),
          tag: "Interior Design",
          title: "Best For Any Office & Business Interior Solution",
          date: "25 December, 2022 ",
        },
      ],
    };
  },
  components: { ItemListComponent, PaginationComponent },
};
</script>

<style scoped></style>
