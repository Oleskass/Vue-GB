<template>
  <header class="header center">
    <div class="header__logo">
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
    <div class="nav">
      <div class="nav__links">
        <a href="index.html" class="nav__link">Home</a>
      </div>
      <div class="nav_links">
        <a href="#" class="nav__link">Project</a>
      </div>
      <div class="nav_links">
        <a href="blog.html" class="nav__link">Blog</a>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$widthContent: 1200px;
$textColorTitle: #292f36;
$textColorDescr: #4d5053;

.header {
  display: flex;
  justify-content: space-between;
  margin-top: 53px;
  margin-bottom: 53px;
  .nav {
    display: flex;
    gap: 50px;
    align-items: center;
    &__link {
      color: $textColorTitle;
      text-align: center;
      font-family: Jost;
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 125%; /* 25px */
    }
  }
}
</style>
