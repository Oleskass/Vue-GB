<template>
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Articles</title>
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
        <section class="banner__blog banner__blog__articles"></section>

        <section class="articles center">
          <div class="articles__box">
            <div v-for="article in currentArticle" :key="article.id">
              <h2 class="articles__box__title">{{ article.title }}</h2>
              <img
                class="articles__box__img"
                :src="article.img"
                alt="picture"
              />
              <div class="articles__box__date-nav">
                <p class="articles__box__date">{{ article.date }}</p>
                <ul class="articles__box__nav">
                  <li class="articles__box__nav-link">Interior /</li>
                  <li class="articles__box__nav-link">Home /</li>
                  <li class="articles__box__nav-link">Decor</li>
                </ul>
              </div>
              <p class="articles__box__text">{{ article.text }}</p>
              <div class="articles__box__quote">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="74"
                  height="56"
                  fill="none"
                >
                  <path
                    fill="#CDA274"
                    d="M58.252.6c4.4 0 8 1.467 10.8 4.4 2.666 2.933 4 6.867 4 11.8 0 8.667-2.867 16.2-8.6 22.6-5.867 6.4-12.867 11.667-21 15.8l-2-3.4c3.333-2.133 6.466-4.867 9.4-8.2 2.8-3.333 5-6.933 6.6-10.8l-5.6-4.2c-2.267-1.467-4.134-3.467-5.6-6-1.467-2.4-2.2-4.733-2.2-7 0-4.267 1.333-7.867 4-10.8C50.585 2 53.985.6 58.252.6Zm-41.2 0c4.4 0 8 1.467 10.8 4.4 2.666 2.933 4 6.867 4 11.8 0 8.667-2.867 16.2-8.6 22.6-5.867 6.4-12.867 11.667-21 15.8l-2-3.4c3.333-2.133 6.466-4.867 9.4-8.2 2.8-3.333 5-6.933 6.6-10.8l-5.6-4.2c-2.267-1.467-4.134-3.467-5.6-6-1.467-2.4-2.2-4.733-2.2-7 0-4.267 1.333-7.867 4-10.8C9.385 2 12.785.6 17.052.6Z"
                  />
                </svg>
                <p>{{ article.quote }}</p>
              </div>
            </div>
          </div>

          <div class="articles__tags">
            <h3 class="articles__tags__title">Tags</h3>
            <div class="articles__tags__btns">
              <button
                class="articles__tags__btn"
                @click="chooseArticle(nameTag)"
                v-for="nameTag in tags"
                :key="nameTag.id"
              >
                {{ nameTag }}
              </button>
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
      tags: [
        "Kitchen",
        "Bedroom",
        "Building",
        "Architecture",
        "Kitchen Planning",
        "Bedroom Planning",
      ],
      articles: [
        {
          title: "Let’s Get Solution For Building Construction Work",
          img: require("../assets/img/article__img1.png"),
          date: "26 December, 2022",
          text: "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable. Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          quote: "The details are not the details. They make the design.",
          tag: "Kitchen",
        },
        {
          title: "Design sprints are great",
          img: require("../assets/img/article__img2.png"),
          date: "20 December,2022",
          text: "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          quote: "Contrary to popular belief.",
          tag: "Kitchen",
        },
        {
          title: "Nisi, ullam neque",
          img: require("../assets/img/article__img5.jpeg"),
          date: "02 June, 2023",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nisi, ullam neque. Nostrum ea veritatis maxime accusantium est, sit dignissimos doloribus numquam eum laboriosam enim dolores ut, suscipit libero molestias inventore sapiente laudantium similique cumque praesentium eos delectus. Consequatur nam explicabo et consequuntur porro vel rerum. Eaque nihil consectetur voluptas quidem delectus omnis natus corrupti, officiis perspiciatis velit maxime laborum explicabo!",
          quote: "Tmaxime laborum explicabo!",
          tag: "Architecture",
        },
        {
          title: "Iusto minima beatae alias",
          img: require("../assets/img/article__img7.avif"),
          date: "12 December, 2022",
          text: "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable. Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          quote: "The details are not the details. They make the design.",
          tag: "Kitchen Planning",
        },
        {
          title: "Ex illum magni laudantium",
          img: require("../assets/img/article__img4.jpeg"),
          date: "26 November, 2022",
          text: "Vero voluptates odio magni quis quod ea iusto praesentium provident ad mollitia perferendis, et unde maiores velit a modi! Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable. Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          quote: "The details are not the details. They make the design.",
          tag: "Building",
        },
        {
          title: "Voluptatibus modi, tempore omnis, fugit illum",
          img: require("../assets/img/article__img3.jpeg"),
          date: "06 May, 2022",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex itaque obcaecati. Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable. Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          quote: "Voluptatibus modi, tempore omnis",
          tag: "Bedroom",
        },
        {
          title: "Lorem ipsum dolor sit amet consectetur",
          img: require("../assets/img/article__img6.jpeg"),
          date: "29 December, 2022",
          text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem fugiat porro eos modi sed quidem quasi illo enim corrupti, quae earum explicabo culpa, atque quo expedita incidunt molestias, accusamus assumenda impedit quis praesentium odit rerum. Perferendis, repudiandae id quo corporis eligendi laudantium sit et ipsam temporibus culpa vitae? Blanditiis beatae deserunt ullam. Dicta maxime ea atque molestiae delectus, eligendi error?",
          quote:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. In, vitae!",
          tag: "Bedroom Planning",
        },
      ],
      currentArticle: [
        {
          title: "Let’s Get Solution For Building Construction Work",
          img: require("../assets/img/article__img1.png"),
          date: "26 December, 2022",
          text: "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable. Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          quote: "The details are not the details. They make the design.",
          tag: "Kitchen",
        },
        {
          title: "Design sprints are great",
          img: require("../assets/img/article__img2.png"),
          date: "20 December,2022",
          text: "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          quote: "Contrary to popular belief.",
          tag: "Kitchen",
        },
        {
          title: "Nisi, ullam neque",
          img: require("../assets/img/article__img5.jpeg"),
          date: "02 June, 2023",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nisi, ullam neque. Nostrum ea veritatis maxime accusantium est, sit dignissimos doloribus numquam eum laboriosam enim dolores ut, suscipit libero molestias inventore sapiente laudantium similique cumque praesentium eos delectus. Consequatur nam explicabo et consequuntur porro vel rerum. Eaque nihil consectetur voluptas quidem delectus omnis natus corrupti, officiis perspiciatis velit maxime laborum explicabo!",
          quote: "Tmaxime laborum explicabo!",
          tag: "Architecture",
        },
        {
          title: "Iusto minima beatae alias",
          img: require("../assets/img/article__img7.avif"),
          date: "12 December, 2022",
          text: "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable. Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          quote: "The details are not the details. They make the design.",
          tag: "Kitchen Planning",
        },
        {
          title: "Ex illum magni laudantium",
          img: require("../assets/img/article__img4.jpeg"),
          date: "26 November, 2022",
          text: "Vero voluptates odio magni quis quod ea iusto praesentium provident ad mollitia perferendis, et unde maiores velit a modi! Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable. Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          quote: "The details are not the details. They make the design.",
          tag: "Building",
        },
        {
          title: "Voluptatibus modi, tempore omnis, fugit illum",
          img: require("../assets/img/article__img3.jpeg"),
          date: "06 May, 2022",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex itaque obcaecati. Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable. Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          quote: "Voluptatibus modi, tempore omnis",
          tag: "Bedroom",
        },
        {
          title: "Lorem ipsum dolor sit amet consectetur",
          img: require("../assets/img/article__img6.jpeg"),
          date: "29 December, 2022",
          text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem fugiat porro eos modi sed quidem quasi illo enim corrupti, quae earum explicabo culpa, atque quo expedita incidunt molestias, accusamus assumenda impedit quis praesentium odit rerum. Perferendis, repudiandae id quo corporis eligendi laudantium sit et ipsam temporibus culpa vitae? Blanditiis beatae deserunt ullam. Dicta maxime ea atque molestiae delectus, eligendi error?",
          quote:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. In, vitae!",
          tag: "Bedroom Planning",
        },
      ],
    };
  },

  methods: {
    chooseArticle(tag) {
      this.currentArticle = this.articles.filter((el) => el.tag === tag);
    },
  },
};
</script>

<style scoped></style>
