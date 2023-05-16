<template>
   <div class="border border-gray-200 shadow-xl py-12 px-10">
     <div class="overflow-hidden w-14 h-14 block mb-4">
        <img :src="icon" class="mx-auto w-full">
     </div>
     <h1 class="font-bold text-2xl text-black  uppercase mb-4">{{title}}</h1>
     <h1 class="text-black ">{{desc}}</h1>
   </div>
</template>

<script>
export default {
 props:{
    icon:String,
    title:String,
    desc:String,
 }
}
</script>

<style>

</style>