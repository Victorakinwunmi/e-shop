<template>
  <div class="fixed z-10">
    <div class="lg:block w-full bg-white shadow-xl lg:shadow-sm rounded-b-md py-5 z-10 fixed">
      <div class="flex justify-between items-center max-w-8xl mx-auto px-4 md:px-6 py-2 lg:px-2 xl:px-0">
        <ul class="items-center gap-10 hidden lg:flex">
          <li class="uppercase text-sm">how it works</li>
          <li class="uppercase text-sm">Faqs</li>
        </ul>
        <div
          :class="is_revealed ? 'hidden' : 'block lg:hidden'"
          @click="showMenu"
          class=""
        >
          <div class="">
            <img :src="require('@/assets/icons/open_menu.png')" class="h-10 w-10">
          </div>
        </div>
        <div
          :class="is_revealed ? 'block' : 'hidden'"
          @click="hideMenu"
          class=""
        >
          <div class="">
            <img :src="require('@/assets/icons/close_menu.png')" class="h-10 w-10">
          </div>
        </div>
        <div class="">
          <img :src="require('@/assets/images/b_logo.svg')" class="w-20 h-15">
        </div>

        <div class="flex items-center">
          <img :src="require('@/assets/icons/search.png')" class="mr-2 lg:mr-4 w-6 h-6">
          <h1 class="uppercase text-sm hidden lg:block">sign in/<span>register</span></h1>
        </div>
      </div>
    </div>
      <div :class="is_revealed ? 'block h-screen' : 'hidden lg:block' " class="w-full mt-20 lg:mt-24 shadow-md border border-gray-200 bg-gray-50 py-6 z-10 fixed">
        <ul class=" block lg:flex justify-center">
          <li class="px-4 uppercase text-sm lg:text-xs py-4 lg:py-0 hover:text-gray-400 cursor-pointer ">what's new</li>
          <li class="px-4 uppercase text-sm lg:text-xs py-4 lg:py-0 hover:text-gray-400 cursor-pointer ">designers</li>
          <li class="px-4 uppercase text-sm lg:text-xs py-4 lg:py-0 hover:text-gray-400 cursor-pointer ">collections</li>
          <li class="px-4 uppercase text-sm lg:text-xs py-4 lg:py-0 hover:text-gray-400 cursor-pointer ">dresses</li>
          <li class="px-4 uppercase text-sm lg:text-xs py-4 lg:py-0 hover:text-gray-400 cursor-pointer ">shoes</li>  
          <li class="px-4 uppercase text-sm lg:text-xs py-4 lg:py-0 hover:text-gray-400 cursor-pointer ">accessories</li>
          <li class="px-4 uppercase text-sm lg:text-xs py-4 lg:py-0 hover:text-gray-400 cursor-pointer ">bags</li>
          <li class="px-4 uppercase text-sm lg:text-xs py-4 lg:py-0 hover:text-gray-400 cursor-pointer ">lenders</li>  
        </ul>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      is_revealed: false,
    };
  },
  methods: {
    showMenu() {
      this.is_revealed = true;
    },
    hideMenu() {
      this.is_revealed = false;
    },
  },
};
</script>

<style>
 
 @media screen and (min-width:1024px)
  { 
    .max-w-8xl{
    width: 75%;
  }
  }
</style>