<template>
  <!-- <router-view/> -->
  <div class="container">
    <Navbar />
    <TextEditorBody />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import TextEditorBody from "@/components/TextEditorBody.vue";


export default {
  name: "App",
  components: {
    Navbar,
    TextEditorBody
  }
}
</script>

<style lang="scss" scoped>

</style>