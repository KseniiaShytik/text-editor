<template>
  <div @click="isSelect = !isSelect" :class="{active: isSelect}" class="size-wrap">
    <p>Size</p>
    <img v-if="!isSelect" class="arrow" src="@/assets/arrow-down.svg" alt="arrow down">
    <img v-else class="arrow" src="@/assets/arrow-up-white.svg" alt="arrow down">
    <!-- DROPDOWN -->
    <div class="dropdown-menu">
      <ul>
        <li class="submenu size-1">Normal text</li>
        <li class="submenu size-2">Heading 1</li>
        <li class="submenu size-3">Heading 2</li>
        <li class="submenu size-4">Heading 3</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Size",
  data() {
    return {
      isSelect: false,
    }
  } ,
  methods: {
    
  },
}
</script>

<style lang="scss">
.size-wrap {
  display: flex;
  gap: 6px;
  padding: 8px 10px;
  &.active {
    background-color: #38618c;
    .dropdown-menu { display: block; }
  }
    p { 
      cursor: default;
      margin: 0; 
    }
    .arrow { cursor: pointer; }
}

.dropdown-menu {
  display: none;
  .submenu {
    list-style-type: none;
    cursor: pointer;
    padding: 6px;
    &:hover {
      border: 1px solid blue;
    }
  }
  .size-1 { 
  
    font-size: 16px; 
    color: #99d98c;
  }
  .size-2 { 
    font-size: 2em; 
    color: #38618c;
  }
  .size-3 { 
    font-size: 1.5em;
    color: #f06688; 
  }
  .size-4 { 
    font-size: 1.17em; 
    color: #fc9727;
  }
}
</style>