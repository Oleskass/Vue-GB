<template>
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Blog</title>
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
        <section class="banner__blog banner">
          <div class="banner__box">
            <h2 class="banner__heading">Articles & News</h2>
            <div class="banner__nav">
              <a href="index.html">Home</a>
              /
              <a href="blog.html">Blog</a>
            </div>
          </div>
        </section>

        <section class="blog flex-start">
          <div class="blog__latest center">
            <h2 class="blog__latest__title">Latest Post</h2>
            <div class="blog__latest__box">
              <img
                src="../assets/img/latest_img.png"
                alt="picture"
                class="blog__latest__img"
              />
              <div class="blog__latest__descr">
                <h3 class="blog__latest__descr__title">
                  Low Cost Latest Invented Interior Designing Ideas
                </h3>
                <p class="blog__latest__descr__text">
                  Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae
                  turpis dignissim maximus.posuere in.Contrary to popular
                  belief.
                  <br />
                  <br />
                  Lorem Ipsum is not simply random text. It has roots in a piece
                  of classica.
                </p>
                <div class="blog__items__sub">
                  <div class="blog__items__sub__date">26 December,2022</div>
                  <div class="blog__items__sub__btn">
                    <a href="articles.html">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="52"
                        height="53"
                        fill="none"
                      >
                        <circle cx="26" cy="26.267" r="26" fill="#F4F0EC" />
                        <path
                          stroke="#292F36"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="m23.771 32.953 5.943-6.686-5.943-6.686"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="blog__heading center">
            <h2 class="blog__heading__title">Articles & News</h2>
          </div>
          <div class="blog__content center">
            <div
              class="blog__items"
              v-for="(card, index) in cards"
              :key="index"
            >
              <div class="blog__items__img blog__items__img1">
                <img :src="card.img" alt="blog_item_img" />
              </div>
              <div class="blog__items__descr">
                <h3 class="blog__items__title">{{ card.title }}</h3>
                <div class="blog__items__sub">
                  <div class="blog__items__sub__date">{{ card.date }}</div>
                  <div class="blog__items__sub__btn">
                    <a href="articles.html">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="52"
                        height="53"
                        fill="none"
                      >
                        <circle
                          class="circleBtn"
                          cx="26"
                          cy="26.267"
                          r="26"
                          fill="#F4F0EC"
                        />
                        <path
                          stroke="#292F36"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="m23.771 32.953 5.943-6.686-5.943-6.686"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
              </div>
              <div class="blog__items__tag">
                <p class="blog__items__tag__text">{{ card.tag }}</p>
              </div>
            </div>
          </div>
        </section>
      </div>
    </body>
  </html>
</template>

<script>
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
};
</script>

<style scoped></style>
