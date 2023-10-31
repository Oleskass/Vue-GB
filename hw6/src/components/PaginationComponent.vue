<template>
  <div class="pagination__element" v-for="(page, index) in pages" :key="index">
    <svg xmlns="http://www.w3.org/2000/svg" width="53" height="52" fill="none">
      <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
    </svg>
    <p>{{ page }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pages: ["01", "02", "03", ">"],
    };
  },
};
</script>

<style lang="scss" scoped>
.pagination__element {
  position: relative;
  color: #292f36;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 150%; /* 24px */
  text-transform: capitalize;
  cursor: pointer;
  & p {
    position: absolute;
    top: 14px;
    left: 17px;
  }
  &:hover svg {
    fill: #f4f0ec;
    & circle {
      stroke: #f4f0ec;
    }
  }
}
</style>
