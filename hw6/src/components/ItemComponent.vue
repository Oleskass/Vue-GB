<template>
  <div class="project__card">
    <div class="project__img">
      <img :src="item.image" alt="project__img" />
    </div>
    <div class="project__item__descr">
      <div class="project__item__descr__left">
        <h3 class="project__item__title">{{ item.heading }}</h3>
        <p class="project__item__text">{{ item.descr }}</p>
      </div>
      <div class="project__item__descr__btn">
        <a href="#">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="70"
            height="70"
            fill="none"
          >
            <circle cx="35" cy="35" r="35" fill="#F4F0EC" />
            <path
              stroke="#292F36"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="m32 44 8-9-8-9"
            />
          </svg>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: Object,
  },
};
</script>

<style lang="scss" scoped>
.project {
  &__card {
    max-width: 500px;
    margin-bottom: 9px;
    position: relative;
    &::after {
      position: absolute;
      top: 5px;
      right: 0;
      content: url(../assets/img/star_img.svg);
      cursor: pointer;
      &:hover svg {
        fill: #ffa928;
        // stroke: #ffa928;
      }
    }
  }
  &__img {
    margin-bottom: 28px;
  }
  &__item__descr {
    align-items: center;
  }
}
</style>
