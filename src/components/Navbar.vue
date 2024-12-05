<template>
    <div class="container">
        <div class="arrows">
        <Rollback/>
        <Revert/>
        </div>
        <Size/>
        <Location/>
        <Color/>
        <Bold/>
        <Cursive/>
        <Underline/>
        <Strikethrough/>
        <Code />
        <Clear/>
        <UnorderedList/>
        <OrderedList/>
        <Link/>
        <Image/>
    </div>
    
</template>

<script>
import Rollback from "@/components/Rollback.vue";
import Revert from "@/components/Revert.vue";
import Size from "@/components/SizeText.vue";
import Location from "@/components/LocationText.vue";
import Color from "@/components/Color.vue";
import Bold from "@/components/Bold.vue";
import Cursive from "@/components/Cursive.vue";
import Underline from "@/components/Underline.vue";
import Strikethrough from "@/components/Strikethrough.vue";
import Clear from "@/components/Clear.vue";
import Code from "@/components/Code.vue";
import UnorderedList from "@/components/UnorderedList.vue";
import OrderedList from "@/components/OrderedList.vue";
import Link from "@/components/Link.vue";
import Image from "@/components/Image.vue";

export default {
    components: {
        Rollback,
        Revert,
        Size,
        Location,
        Color,
        Bold,
        Cursive,
        Underline,
        Strikethrough,
        Clear,
        Code,
        UnorderedList,
        OrderedList,
        Link,
        Image,
    }
}
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  gap: 30px;
  align-items: center;
  font-family: 'Courier New', Courier, monospace;
}
 .arrows {
    display: flex;
    gap: 6px;
  }
</style>