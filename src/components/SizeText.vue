<template>
    <div class="size-wrap">
      <p>Size</p>
      <img @click="chooseSize" class="arrow" src="@/assets/arrow-down.svg" alt="arrow down">
    </div>
</template>

<script>
export default {
  name: "Size",
  methods: {
    chooseSize() {
      const size = document.querySelector(".size-wrap");
      size.style.backgroundColor = "blue";
      // const arrowBlack = document.querySelector(".arrow");
      // arrowBlack.delete
      return 
    } //add size for text
  },
}
</script>

<style lang="scss">
.size-wrap {
    display: flex;
    gap: 6px;
    padding: 8px 10px;

    p { 
      cursor: default;
      margin: 0; 
    }
    .arrow { cursor: pointer; }
}
</style>