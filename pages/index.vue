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
    <div class="py-16 lg:py-28 max-w-8xl mx-auto px-2 lg:px-8 xl:px-0">
       <h1 class="uppercase text-center mb-5 text-2xl">just landed</h1>
       <div class="flex mb-5 items-center justify-between">
         <img :src="require('@/assets/icons/leftchev.png')" class="w-10 cursor-pointer" @click="showPrev">
         <img :src="require('@/assets/icons/rightchev.png')" class="w-10 cursor-pointer" @click="showNext">
       </div>
      <VueSlickCarousel v-bind="settings" ref="carousel" >
          <div>
              <div class="bg-no-repeat bg-cover mx-2 bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/images/cta.png')+ ')' } ">
                <div class="bg-black h-96 justify-end flex bg-opacity-10 flex-col">
                  <div class="bg-black bg-opacity-50 py-4 px-6">
                     <h1 class="text-white font-bold text-xl">lorem ipsum</h1>
                     <h1  class="text-white mt-2">2000</h1>
                  </div>
                </div>
              </div>
          </div>
          <div>
              <div class="bg-no-repeat bg-cover mx-2 bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/images/cta3.png')+ ')' } ">
                <div class="bg-black h-96 flex-col justify-end flex bg-opacity-10">
                  <div class="bg-black bg-opacity-50 py-4 px-6">
                    <h1 class="text-white font-bold text-xl">lorem ipsum</h1>
                     <h1  class="text-white mt-2">2000</h1>
                  </div>
                </div>
              </div>
          </div>
          <div>
              <div class="bg-no-repeat bg-cover mx-2 bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/images/cta.png')+ ')' } ">
                <div class="bg-black h-96 flex-col justify-end flex bg-opacity-10">
                  <div class="bg-black bg-opacity-50 py-4 px-6">
                    <h1 class="text-white font-bold text-xl">lorem ipsum</h1>
                     <h1  class="text-white mt-2">2000</h1>
                  </div>
                </div>
              </div>
          </div>
          <div>
              <div class="bg-no-repeat bg-cover mx-2 bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/images/cta2.png')+ ')' } ">
                <div class="bg-black h-96 flex-col justify-end flex bg-opacity-10">
                  <div class="bg-black bg-opacity-50 py-4 px-6">
                     <h1 class="text-white font-bold text-xl">lorem ipsum</h1>
                     <h1  class="text-white mt-2">2000</h1>
                  </div>
                </div>
              </div>
          </div>
          <div>
              <div class="bg-no-repeat bg-cover mx-2 bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/images/cta3.png')+ ')' } ">
                <div class="bg-black h-96 flex-col justify-end flex bg-opacity-10">
                  <div class="bg-black bg-opacity-50 py-4 px-6">
                     <h1 class="text-white font-bold text-xl">lorem ipsum</h1>
                     <h1  class="text-white mt-2">2000</h1>
                  </div>
                </div>
              </div>
          </div>
      </VueSlickCarousel>
    </div>
    <div class="py-8 px-2 lg:px-6 xl:px-0 lg:py-4 mb-8 lg:mb-16 max-w-8xl mx-auto">
      <h1 class="uppercase mb-8 text-2xl text-center">why us</h1>
      <div class=" grid grid-cols-1 lg:grid-cols-3 gap-4 mx-auto">
         <ItemsCard v-for="item in services" :key="item.id" 
            :icon="item.icon"
            :title="item.title"
            :desc="item.desc"
          />
      </div>
    </div>

    <div class="block lg:flex py-8 lg:py-16 max-w-8xl mx-auto px-2 gap-4 lg:px-8 xl:px-0">
      <div class="w-full lg:w-6/12 bg-gray-50">
        <img :src="require('@/assets/images/cta3.png')" class="mx-auto">
      </div>
      <div class="w-full lg:w-6/12 bg-gray-100 mt-4 lg:mt-0 py-5 px-8 lg:py-16 lg:px-10">
        <h1 class="uppercase text-2xl font-semibold">laptop collection!</h1>
        <p class="mt-2">Lorem, ipsum dolor sit amet consectetur adipisicing elit</p>
        <div class="flex items-center gap-2 mt-4 lg:mt-10">
           <button class="font-semibold">Check out</button>
           <img :src="require('@/assets/icons/right.png')" class="w-8 h-8"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'

export default {
  name: 'MyComponent',
  components: { VueSlickCarousel },
  data(){
    return{
      settings:{
       "centerMode": true,
       "centerPadding": "200px",
       "focusOnSelect": true,
       "infinite": true,
       "slidesToShow": 3,
       "speed": 500,
       "arrows":false,
       "responsive": [
        {
          "breakpoint": 1024,
          "settings": {
          "centerMode": true,
          "centerPadding": "70px",
          "focusOnSelect": true,
          "infinite": true,
          "slidesToShow": 2,
          "speed": 500,
          "arrows":false,
            
          }
        },
        {
          "breakpoint": 600,
          "settings": {
          "centerMode": true,
          "centerPadding": "20px",
          "focusOnSelect": true,
          "infinite": true,
          "slidesToShow": 2,
          "speed": 500,
          "arrows":false,
            
          }
        },
        {
          "breakpoint": 478,
          "settings": {
          "centerMode": true,
          "centerPadding": "20px",
          "focusOnSelect": true,
          "infinite": true,
          "slidesToShow": 1,
          "speed": 500,
          "arrows":false,
            
          }
        },
       ]
      },
      services:[
        {
          id:1,
          icon:require('@/assets/icons/icon1.png'),
          title:'Lorem',
          desc:`Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem fugit voluptatem vitae deleniti. Soluta esse,
                earum nobis perferendis ipsum placeat dolorem repellendus iusto
                suscipit mollitia dicta odio totam in. Illo.`
        },
        {
          id:2,
          icon:require('@/assets/icons/icon2.png'),
          title:'ipsum',
          desc:`Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem fugit voluptatem vitae deleniti. Soluta esse,
              earum nobis perferendis ipsum placeat dolorem repellendus iusto
              suscipit mollitia dicta odio totam in. Illo.`
        },
        {
          id:3,
          icon:require('@/assets/icons/icon3.png'),
          title:'remip',
          desc:`Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem fugit voluptatem vitae deleniti. Soluta esse,
                earum nobis perferendis ipsum placeat dolorem repellendus iusto
                suscipit mollitia dicta odio totam in. Illo.`
        },
      ]
      
    };
  },
  methods: {
      showPrev() {
        this.$refs.carousel.prev()
      },
      showNext() {
        this.$refs.carousel.next()
      },
     
  }
}
</script>

<style>

</style>