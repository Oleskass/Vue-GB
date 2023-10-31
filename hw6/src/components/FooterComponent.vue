<template>
  <footer class="footer center">
    <div class="footer__about">
      <div class="footer__logo">
        <a href="index.html" class="logo__link">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="34"
            height="34"
            fill="none"
          >
            <path
              fill="#CDA274"
              d="M0 34h13.459V24.5a3.644 3.644 0 0 1 3.645-3.645 3.644 3.644 0 0 1 3.644 3.645V34h13.25V0C15.22 0 0 15.221 0 34Z"
            />
          </svg>
          <h2 class="logo">Interno</h2>
        </a>
      </div>
      <p class="footer__about__text">
        It is a long established fact that a reader will be distracted lookings.
      </p>
      <div class="footer__about__links">
        <a href="#">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="19"
            height="16"
            fill="none"
          >
            <path
              fill="#292F36"
              d="M16.637 4.594v.492c0 4.887-3.692 10.476-10.477 10.476-2.11 0-4.043-.597-5.66-1.652.281.035.563.07.879.07a7.422 7.422 0 0 0 4.57-1.582c-1.617-.035-2.988-1.09-3.445-2.566.246.035.457.07.703.07.316 0 .668-.07.95-.14A3.696 3.696 0 0 1 1.202 6.14v-.036c.492.282 1.09.422 1.688.457a3.632 3.632 0 0 1-1.653-3.058c0-.703.176-1.336.492-1.863a10.71 10.71 0 0 0 7.63 3.867 3.467 3.467 0 0 1-.106-.844A3.69 3.69 0 0 1 12.945.973c1.055 0 2.004.422 2.707 1.16a7.798 7.798 0 0 0 2.32-.914 3.607 3.607 0 0 1-1.617 2.039 6.918 6.918 0 0 0 2.11-.563 7.818 7.818 0 0 1-1.828 1.899Z"
            />
          </svg>
        </a>
        <a href="#">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="17"
            height="16"
            fill="none"
          >
            <path
              fill="#292F36"
              d="M4.14 16V5.488H.872V16h3.27ZM2.489 4.082c1.055 0 1.899-.879 1.899-1.934 0-1.02-.844-1.863-1.899-1.863-1.02 0-1.863.844-1.863 1.863 0 1.055.844 1.934 1.863 1.934ZM16.34 16h.035v-5.766c0-2.812-.633-4.992-3.938-4.992-1.582 0-2.636.88-3.093 1.688h-.035V5.488h-3.13V16h3.27v-5.203c0-1.371.246-2.672 1.934-2.672 1.687 0 1.723 1.547 1.723 2.777V16h3.234Z"
            />
          </svg>
        </a>
      </div>
    </div>
    <div class="footer__nav">
      <h3 class="footer__title">Pages</h3>
      <a href="#" class="footer__text">Home</a>
      <a href="#" class="footer__text">Project</a>
      <a href="#" class="footer__text">Blog</a>
    </div>
    <div class="footer__contact">
      <h3 class="footer__title">Contact</h3>
      <p class="footer__text footer__text_mod">
        55 East Birchwood Ave. Brooklyn, New York 11201
      </p>
      <p class="footer__text">contact@interno.com</p>
      <p class="footer__text">(123) 456 - 7890</p>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$widthContent: 1200px;
$textColorTitle: #292f36;
$textColorDescr: #4d5053;
.footer {
  padding-bottom: 134px;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 101px;
  &__about {
    display: flex;
    width: 393px;
    flex-direction: column;
    align-items: flex-start;
    gap: 31px;
    &__text {
      color: $textColorDescr;
      font-family: Jost;
      font-size: 22px;
      font-style: normal;
      font-weight: 400;
      line-height: 150%; /* 33px */
      letter-spacing: 0.22px;
    }
    &__links {
      display: flex;
      width: 225px;
      align-items: center;
      gap: 54px;
    }
  }
  &__nav {
    display: flex;
    width: 125px;
    flex-direction: column;
    align-items: flex-start;
    gap: 9px;
  }
  &__title {
    color: $textColorTitle;
    font-size: 25px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%; /* 31.25px */
  }
  &__text {
    color: $textColorDescr;
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 300%; /* 66px */
    letter-spacing: 0.22px;
    &_mod {
      line-height: 150%;
    }
  }
  &__contact {
    display: flex;
    width: 258px;
    flex-direction: column;
    align-items: flex-start;
    gap: 26px;
  }
}
</style>
