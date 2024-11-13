<template>
    
    <div class="relative h-full w-full bg-slate-950 text-white">
    <div class="absolute bottom-0 left-0 right-0 top-0 bg-[linear-gradient(to_right,#4f4f4f2e_1px,transparent_1px),linear-gradient(to_bottom,#4f4f4f2e_1px,transparent_1px)] bg-[size:14px_24px] [mask-image:radial-gradient(ellipse_60%_50%_at_50%_0%,#000_70%,transparent_100%)]"></div>
    <div class="navbar bg-transparent text-primary-content">
        <a href="https://github.com" class="btn btn-ghost text-3xl  text-accent">Murtaja<span class=" uppercase text-neutral-content">api</span></a>
    </div>
    

    <!-- new content -->

    <div v-if="character" class="hero min-h-screen text-black">
        <div class="hero-content flex-col lg:flex-row-reverse">
            <img :src="character.images[0]" class="max-w-lg h-auto rounded-lg shadow-2xl" />
            <div class="">
                <h1 class=" font-bold text-7xl  bg-gradient-to-r via-red-400 from-red-500 to-indigo-600 text-transparent inline-block bg-clip-text ">{{ character.name }}</h1>
                <p class="py-6 text-red-300">
                    {{ character.personal.titles }}  
                </p>
            </div>
        </div>
    </div>

    <div v-else>
    <p>Loading character details...</p>
  </div>

    <!-- old content -->
    <!-- <div v-if="character" class="character-detail">
      <h1>{{ character.name }}</h1>
      <img :src="character.images[0]" alt="character image" />
      <p>Clan: {{ character.personal.clan }}</p>
       Add more character details here as needed 
    </div> -->

    </div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue'
  import { useRoute } from 'vue-router'
  import { useFetch } from '#app'
  
  const route = useRoute()
  const character = ref(null)
  
  onMounted(async () => {
    try {
      const { data } = await useFetch(`https://dattebayo-api.onrender.com/characters/${route.params.id}`)
      character.value = data.value
    } catch (error) {
      console.error('Error fetching character details:', error)
    }
  })
  </script>
  