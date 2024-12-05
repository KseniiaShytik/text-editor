<template>
    <div class="color-wrap">
        <input type="color" name="color" id="color" class="color" v-model="color">
    </div>
</template>

<script>
export default {
  name: "Color",
  data() {
    return {
        color: ''
    }
  }
}
</script>

<style lang="scss">
.color-wrap {
   
    .color {
        width: 20px;
        height: 20px;
        border-radius: 50%;
        padding: 0;
        margin: 0;
        -webkit-appearance: none;
        border: none;
        overflow: hidden;
        outline: none;
        cursor: inherit;
    }
    input[type="color"]::-webkit-color-swatch-wrapper {
        padding: 0;    
    }

    input[type="color"]::-webkit-color-swatch {
        border: none;  
        border-radius: 50%;
    }
}
</style>