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
      <div :class="is_revealed ? 'block h-screen' : 'hidden lg:block' " class="w-full mt-28 lg:mt-24 shadow-md border border-gray-200 bg-gray-50 py-6 z-10 fixed">
        <div class=" grid grid-cols-1 lg:grid-cols-8 gap-4 max-w-2xl mx-auto">
          <div class=" cursor-pointer" @mouseover="drop_down1 = true" @mouseleave="drop_down1 = false">
            <div class="uppercase text-sm lg:text-xs hover:text-gray-400 cursor-pointer border-transparent border-b-2 py-4 duration-500 w-full text-center lg:w-20 ease-in-out hover:border-gray-400">what's new</div>
            <div v-show="drop_down1" class="block lg:absolute items-center gap-10 lg:flex shadow-md left-0 max-w-full">
              <ul v-show="drop_down1" class="w-full lg:w-1/3 block lg:mt-5 bg-white py-5">
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 1</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 2</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 3</a>
              </ul>
              <div class="w-2/3 hidden lg:block">
                <img :src="require('@/assets/images/b_logo.svg')" class="w-96 h-96">
              </div>
            </div>
          </div>
          <div class="  cursor-pointer" @mouseover="drop_down2 = true" @mouseleave="drop_down2 = false">
            <div class="uppercase text-sm lg:text-xs hover:text-gray-400 cursor-pointer border-transparent border-b-2 py-4 duration-500 w-full text-center ease-in-out hover:border-gray-400">designers</div>
            <div v-show="drop_down2" class="block lg:absolute items-center gap-10 lg:flex shadow-md left-0 max-w-full">
              <ul v-show="drop_down2" class="w-full lg:w-1/3 block lg:mt-5 bg-white py-5">
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 1</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 2</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 3</a>
              </ul>
              <div class="w-2/3 hidden lg:block">
                <img :src="require('@/assets/images/b_logo.svg')" class="w-96 h-96">
              </div>
            </div>
          </div>
          <div class="cursor-pointer" @mouseover="drop_down3 = true" @mouseleave="drop_down3 = false">
            <div class="uppercase text-sm lg:text-xs hover:text-gray-400 cursor-pointer border-transparent border-b-2 py-4 duration-500 w-full text-center lg:w-20 ease-in-out hover:border-gray-400">collections</div>
            <div v-show="drop_down3" class="block lg:absolute items-center gap-10 lg:flex shadow-md left-0 max-w-full">
              <ul v-show="drop_down3" class="w-full lg:w-1/3 block lg:mt-5 bg-white py-5">
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 1</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 2</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 3</a>
              </ul>
              <div class="w-2/3 hidden lg:block">
                <img :src="require('@/assets/images/b_logo.svg')" class="w-96 h-96">
              </div>
            </div>
          </div>
          <div class=" cursor-pointer" @mouseover="drop_down4 = true" @mouseleave="drop_down4 = false">
            <div class="uppercase text-sm lg:text-xs hover:text-gray-400 cursor-pointer border-transparent border-b-2 py-4 duration-500 w-full text-center lg:text-left lg:text-center w-20 ease-in-out hover:border-gray-400">dresses</div>
            <div v-show="drop_down4" class="block lg:absolute items-center gap-10 lg:flex shadow-md left-0 max-w-full">
              <ul v-show="drop_down4" class="w-full lg:w-1/3 block lg:mt-5 bg-white py-5">
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 1</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 2</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 3</a>
              </ul>
              <div class="w-2/3 hidden lg:block">
                <img :src="require('@/assets/images/b_logo.svg')" class="w-96 h-96">
              </div>
            </div>
          </div>
          <div class="  cursor-pointer" @mouseover="drop_down5 = true" @mouseleave="drop_down5 = false">
            <div class="uppercase text-sm lg:text-xs hover:text-gray-400 cursor-pointer border-transparent border-b-2 py-4 duration-500 w-full text-center lg:w-20 lg:text-center ease-in-out hover:border-gray-400">shoes</div>
            <div v-show="drop_down5" class="block lg:absolute items-center gap-10 lg:flex shadow-md left-0 max-w-full">
              <ul v-show="drop_down5" class="w-full lg:w-1/3 block lg:mt-5 bg-white py-5">
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 1</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 2</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 3</a>
              </ul>
              <div class="w-2/3 hidden lg:block">
                <img :src="require('@/assets/images/b_logo.svg')" class="w-96 h-96">
              </div>
            </div>
          </div>
          <div class="  cursor-pointer" @mouseover="drop_down6 = true" @mouseleave="drop_down6= false">
            <div class="uppercase text-sm lg:text-xs hover:text-gray-400 cursor-pointer border-transparent border-b-2 py-4 duration-500 w-full text-center lg:w-20 ease-in-out hover:border-gray-400">accessories</div>
            <div v-show="drop_down6" class="block lg:absolute items-center gap-10 lg:flex shadow-md left-0 max-w-full">
              <ul v-show="drop_down6" class="w-full lg:w-1/3 block lg:mt-5 bg-white py-5">
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 1</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 2</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 3</a>
              </ul>
              <div class="w-2/3 hidden lg:block">
                <img :src="require('@/assets/images/b_logo.svg')" class="w-96 h-96">
              </div>
            </div>
          </div>
          <div class="  cursor-pointer" @mouseover="drop_down7 = true" @mouseleave="drop_down7 = false">
            <div class="uppercase text-sm lg:text-xs hover:text-gray-400 cursor-pointer border-transparent border-b-2 py-4 duration-500 w-full  lg:w-20 text-center ease-in-out hover:border-gray-400">bags</div>
            <div v-show="drop_down7" class="block lg:absolute items-center gap-10 lg:flex shadow-md left-0 max-w-full">
              <ul v-show="drop_down7" class="w-full lg:w-1/3 block lg:mt-5 bg-white py-5">
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 1</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 2</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 3</a>
              </ul>
              <div class="w-2/3 hidden lg:block">
                <img :src="require('@/assets/images/b_logo.svg')" class="w-96 h-96">
              </div>
            </div>
          </div>
          <div class="cursor-pointer" @mouseover="drop_down8 = true" @mouseleave="drop_down8 = false">
            <div class="uppercase text-sm lg:text-xs hover:text-gray-400 cursor-pointer border-transparent border-b-2 py-4 duration-500 w-full text-center lg:w-20 ease-in-out hover:border-gray-400">lenders</div>
            <div v-show="drop_down8" class="block lg:absolute items-center gap-10 lg:flex shadow-md left-0 max-w-full">
              <ul v-show="drop_down8" class="w-full lg:w-1/3 block lg:mt-5 bg-white py-5">
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 1</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 2</a>
                <a href="/" class="w-full border-transparent block py-2 lg:py-4 border px-2 lg:px-10 hover:border-gray-500 lg:border-0 hover:text-red-500 cursor-pointer">Item 3</a>
              </ul>
              <div class="w-2/3 hidden lg:block">
                <img :src="require('@/assets/images/b_logo.svg')" class="w-96 h-96">
              </div>
            </div>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      is_revealed: false,
      drop_down1: false,
      drop_down2: false,
      drop_down3: false,
      drop_down4: false,
      drop_down5: false,
      drop_down6: false,
      drop_down7: false,
      drop_down8: false,
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
  .max-w-full{
    width: 100%;
  }
</style>