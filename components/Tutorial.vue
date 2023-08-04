<!-- Please remove this file from your project -->
<template>
  <div
    class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0"
  >
    <link
      href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
      rel="stylesheet"
    />
    <div class="max-w-4xl mx-auto sm:px-6 lg:px-8">
      <div class="mt-8 bg-white overflow-hidden shadow sm:rounded-lg p-6">
        <h2 class="text-2xl leading-7 font-semibold">
          Welcome to your Nuxt Application
        </h2>
        <p class="mt-3 text-gray-600">
          We recommend you take a look at the
          <a
            href="https://nuxtjs.org"
            target="_blank"
            class="button--doc text-green-500 hover:underline"
            >Nuxt Documentation</a
          >, whether you are new or have previous experience with the
          framework.<br />
        </p>
        <audio controls autoplay >
          <source src='http://soundbible.com/mp3/Air Plane Ding-SoundBible.com-496729130.mp3' type="audio/mpeg">
        </audio>


        <b-button @click="audioPlay">TEST</b-button>
        <img                  
              :src="require('../assets/gallery0.jpg')"              
            >  
        <p class="mt-4 pt-4 text-gray-800 border-t border-dashed">
          To get started, remove
          <code class="bg-gray-100 text-sm p-1 rounded border"
            >components/Tutorial.vue</code
          >
          and start coding in
          <code class="bg-gray-100 text-sm p-1 rounded border"
            >pages/index.vue</code
          >. Have fun!
        </p>
      </div>
      <div class="flex justify-center pt-4 space-x-2"></div>
    </div>
  </div>
</template>

<script>
const sound = require('../assets/Ring.mp3')
export default {
  name: "NuxtTutorial",
  mounted(){
    console.log(require('../assets/gallery0.jpg'))
  },
  methods:{
    audioPlay(){
      // let audio = new Audio('http://soundbible.com/mp3/Air Plane Ding-SoundBible.com-496729130.mp3')
      console.log(require('../assets/gallery0.jpg'))
      console.log(require('@/sample.mp3'))
      let audio = new Audio('../sample.mp3');
      console.log('audio')
      console.log(audio)
      let playPromise = audio.play();
      if (playPromise !== undefined) {
        playPromise.then(function() {
          console.log("success")
        }).catch(function(error) {
          console.log(error)
          // Automatic playback failed.
          // Show a UI element to let the user manually start playback.
        });
      }
      new Audio(require('@/sample.mp3')).play()
    }
  }
};
</script>
