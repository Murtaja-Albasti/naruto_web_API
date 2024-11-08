<template>
<div class=" mt-36">
    <div class="grid justify-center md:grid-cols-5 grid-cols-3 gap-3">
        <!-- cards -->
        <div v-for="characters in character" :key="characters.id" class="card glass">
            <figure class="w-full">
                <img class="w-full":src="characters.images[0]" alt="car!" />
            </figure>
            <div class="card-body">
                <h2 class="card-title">{{ characters.name }} {{ characters.id }}</h2>
                <p> {{characters.personal.clan}}</p>
            </div>
        </div>
    </div>
</div>
</template>

<script setup>
// https://api.disneyapi.dev/character
// https://api.nekosapi.com/v3
// https://dattebayo-api.onrender.com/characters

import {
    ref
} from 'vue'


const character = ref([])

try {
    const data = await $fetch('https://dattebayo-api.onrender.com/characters')
    character.value = data.characters
    console.log(character.value)
} catch (error) {
    console.error('Error fetching :', error)
}
</script>
