<template>
<div class="relative h-full w-full bg-slate-950 text-white">
    <div class="absolute bottom-0 left-0 right-0 top-0 bg-[linear-gradient(to_right,#4f4f4f2e_1px,transparent_1px),linear-gradient(to_bottom,#4f4f4f2e_1px,transparent_1px)] bg-[size:14px_24px] [mask-image:radial-gradient(ellipse_60%_50%_at_50%_0%,#000_70%,transparent_100%)]"></div>
    <div class="navbar bg-transparent text-primary-content">
        <a href="https://github.com" class="btn btn-ghost text-3xl  text-accent">Murtaja<span class=" uppercase text-neutral-content">api</span></a>
    </div>
    <!-- main part -->
    <div class="hero min-h-screen text-black">
        <div class="hero-content flex-col lg:flex-row-reverse">
            <img src="/img/Gojo Satoru.jpg" class="max-w-sm h-auto rounded-lg shadow-2xl" />
            <div class="">
                <h1 class="text-5xl font-bold text-white">Naruto Simple API</h1>
                <p class="py-6 text-red-300">
                    Naruto Uzumaki (うずまきナルト, Uzumaki Naruto) is a shinobi of Konohagakure's Uzumaki clan. He became the jinchūriki of the Nine-Tails on the day of his birth — a fate that caused him to be shunned by most of Konoha throughout his childhood. After joining Team Kakashi, Naruto worked hard to gain the village's acknowledgement all the while chasing his dream to become Hokage. In the following years, through many hardships and ordeals, he became a capable ninja, regarded as a hero both by the villagers, and soon after, the rest of the world, becoming known as the Hero of the Hidden Leaf (木ノ葉隠れの英雄, Konohagakure no Eiyū, literally meaning: Hero of the Hidden Tree Leaves). He soon proved to be one of the main factors in winning the Fourth Shinobi World War, leading him to achieve his dream and become the village's Seventh Hokage
                </p>
               <NuxtLink :href="`#api`"  > <button v-on:click="" class="btn btn-outline btn-accent">Get Started</button></NuxtLink>
            </div>
        </div>
    </div>

    <div id="api" style="animation-delay: 50ms; transition-delay: 50ms;" class="mt-60 grid grid-rows-1 justify-center">
        <div class=" flex justify-center">
            <h1 class="text-7xl font-bold bg-gradient-to-r via-red-400 from-red-500 to-indigo-600 text-transparent inline-block bg-clip-text ">Animes pictures</h1>
        </div>
        <Api />
    </div>
</div>
</template>


<style>
html{
    scroll-behavior: smooth;
}
</style>