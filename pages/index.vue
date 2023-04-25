<template>
  <div>
    <Container/>
    <div class="lg:px-8 xl:px-0">
      <div class="bg-gray-100 pt-48 block lg:pb-0 lg:flex items-center max-w-8xl mx-auto lg:pt-48 xl:pb-0 px-8 lg:px-4 xl:pr-0 xl:pl-16 ">
        <div class="w-full lg:w-3/6">
          <h1 class="block text-center lg:hidden text-gray-600 text-4xl w-full lg:text-6xl font-bold uppercase">easy comfortable & responsive</h1>
          <h1 class="hidden lg:block text-gray-600 text-4xl max-w-sm lg:text-6xl font-bold uppercase">easy comfortable & responsive</h1>
          <button class="uppercase hidden border hover:bg-black rounded-md hover:text-white duration-500 ease-in-out border-black lg:block mt-8 py-2 px-4 lg:mt-10">learn more</button>
        </div>
        <div class="hidden lg:block lg:w-3/6">
          <img :src="require('@/assets/images/cta2.png')" class="w-full h-full">
        </div>
        <div class="block mt-10 md:mt-16 lg:hidden w-full">
          <img :src="require('@/assets/images/ctasmall.png')" class="w-full">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>