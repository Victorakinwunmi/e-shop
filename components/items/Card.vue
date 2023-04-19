<template>
   <div class="border border-black py-10 px-5">
     <div class="overflow-hidden w-32 h-32 block mb-4">
        <img :src="img" class="mx-auto w-full">
     </div>
     <h1 class="font-bold text-2xl uppercase mb-4">{{title}}</h1>
     <h1>${{price}}</h1>
   </div>
</template>

<script>
export default {
 props:{
    img:String,
    title:String,
    price:Number,
 }
}
</script>

<style>

</style>