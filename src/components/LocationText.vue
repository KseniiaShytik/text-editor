<template>
    <div class="location-wrap">
        <img src="@/assets/location.svg" alt="location text">
        <img class="arrow" src="@/assets/arrow-down.svg" alt="arrow down">
    </div>
</template>

<script>
export default {
  name: "Location",
}
</script>

<style lang="scss">
.location-wrap {
    display: flex;
    gap: 6px;

    img { cursor: default; }
    .arrow { cursor: pointer; }
}
</style>