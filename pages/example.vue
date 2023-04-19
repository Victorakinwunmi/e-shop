<template>
  <div class="flex">
    <div class="relative" @mouseover="showMenu = true" @mouseleave="showMenu = false">
    <button>Dropdown Menu</button>
     <ul v-show="showMenu" class="absolute left-0 z-10 mx-0 border border-gray-100">
      <a href="/" class="py-8 px-12 cursor-pointer">Item 1</a>
      <li class="py-8 px-12 cursor-pointer">Item 2</li>
      <li class="py-8 px-12 cursor-pointer">Item 3</li>
    </ul>
  </div>
  <div class="relative" @mouseover="showMenu2 = true" @mouseleave="showMenu2 = false">
    <button>Dropdown Menu</button>
    <div  v-show="showMenu2" class="w-full">
     <ul class="absolute z-10 left-0 mx-0 border border-gray-100">
      <li class="py-8 px-12 cursor-pointer">Item 1</li>
      <li class="py-8 px-12 cursor-pointer">Item 2</li>
      <li class="py-8 px-12 cursor-pointer">Item 3</li>
     </ul>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
      showMenu2: false,
    };
  }
};
</script>

<style>
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown button {
  background-color: #fff;
  color: #333;
  border: 1px solid #ccc;
  padding: 8px 12px;
  font-size: 16px;
  cursor: pointer;
}

.dropdown ul {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1;
  background-color: #fff;
  border: 1px solid #ccc;
  padding: 8px 0;
  list-style: none;
  margin: 0;
  width: 100%;
}

.dropdown ul li {
  padding: 8px 12px;
  cursor: pointer;
}

.dropdown ul li:hover {
  background-color: #f1f1f1;
}
</style>
