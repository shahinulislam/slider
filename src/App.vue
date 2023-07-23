<script setup>
 import {ref, reactive} from 'vue'

  const fullImage = ref('/img/slider1.jpg')

 const images = [
  {
    thum: "/img/slider1.jpg",
    full: "/img/slider1.jpg"
  },

  {
    thum: "/img/slider2.jpg",
    full: "/img/slider2.jpg"
  },

  {
    thum: "/img/slider3.jpg",
    full: "/img/slider3.jpg"
  },

  {
    thum: "/img/slider4.jpg",
    full: "/img/slider4.jpg"
  },

  {
    thum: "/img/slider5.jpg",
    full: "/img/slider5.jpg"
  },

  {
    thum: "/img/slider6.jpg",
    full: "/img/slider6.jpg"
  },

  {
    thum: "/img/slider7.jpg",
    full: "/img/slider7.jpg"
  }

 ]

 function setImage(image){
  fullImage.value = image.full
 }
</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-5"> VUE3 Slider </h1>
    <div>
      <div class="mb-5">
        <img class="cursor-pointer ring-pink-400 ring-4 ring-offset-4 w-full" :src="fullImage">
      </div>

      <div class="flex space-x-2">
        <img @click="setImage(image)" class="cursor-pointer sm:w-40 rounded-full w-12" v-for="image in images" :src="image.thum">
      </div>

    </div>
  </section>
</template>

<style scoped>

</style>
