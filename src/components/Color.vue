<template>
    <div class="color-wrap">
        <div class="color"></div>
        <img src="@/assets/arrow-down.svg" alt="arrow down">
    </div>
</template>

<script>
export default {
  name: "Color",
}
</script>

<style lang="scss">
.color-wrap {
    display: flex;
    gap: 6px;

    .color {
        width: 20px;
        height: 20px;
        border-radius: 4px;
        background-color: #1F2544;
    }
    img { cursor: pointer; }
}
</style>