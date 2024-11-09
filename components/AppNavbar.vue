<script setup lang="ts">
import { ref } from 'vue';

const isMenuHidden = ref(true);

const toggleMenu = () => {
    isMenuHidden.value = !isMenuHidden.value;
};

const closeMenu = () => {
    isMenuHidden.value = true;
};

const linkClick = () => {
    closeMenu();
    window.scrollTo({ top: 0 });
};

// Definiraj linkove u nizu
const leftLinks = [
    { text: 'Početna', to: '/' },
    { text: 'Utakmice', to: '/services' }
];

const rightLinks = [
    { text: 'Kupite Duks', to: '/pricing' },
    // { text: 'Blog', to: '/blog' },
    { text: 'FAQ', to: '/faq' }
];
</script>

<template>
    <div class="mx-auto fixed w-full bg-blue-800 z-50 p-3 font-lato text-white">
        <nav class="flex container items-center justify-between">
            <!-- Lijevi dio navigacije -->
            <ul class="hidden md:flex gap-6 text-lg">
                <li v-for="link in leftLinks" :key="link.to">
                    <NuxtLink @click="linkClick" :to="link.to">{{ link.text }}</NuxtLink>
                </li>
            </ul>
            
            <!-- Srednji dio za naziv i logo -->
            <NuxtLink to="/" class="flex items-center gap-2">
                <img class="w-12" src="/public/fkjanosik-logo.png" alt="FK Janosik logo"/>
                <span class="text-3xl font-bold">FK Janošik</span>
            </NuxtLink>

            <!-- Desni dio navigacije -->
            <ul class="hidden md:flex gap-6 text-lg">
                <li v-for="link in rightLinks" :key="link.to">
                    <NuxtLink @click="linkClick" :to="link.to">{{ link.text }}</NuxtLink>
                </li>
            </ul>

            <!-- Ikonica za mobilni meni -->
            <span @click="toggleMenu" class="md:hidden right-6 top-2.5 cursor-pointer text-3xl z-10 p-2">
                <svg v-if="isMenuHidden" width="30px" height="30px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M5 14L18 14" stroke="white" stroke-width="1.5" stroke-linecap="round"/>
                    <path d="M5 10L18 10" stroke="white" stroke-width="1.5" stroke-linecap="round"/>
                </svg>
                <svg v-else xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="white" class="w-8 h-8">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/>
                </svg>
            </span>
        </nav>

        <!-- Mobilni meni -->
        <transition name="slide-fade">
            <div v-if="!isMenuHidden" class="absolute bg-blue-800 w-full top-[100%] left-0 z-50 px-10 transform transition-transform duration-500 py-4">
                <ul class="flex flex-col items-center text-white font-light text-lg">
                    <li v-for="link in [...leftLinks, ...rightLinks]" :key="link.to">
                        <NuxtLink @click="linkClick" :to="link.to" class="block px-4 py-2 hover:bg-blue-700 transition-opacity duration-300">{{ link.text }}</NuxtLink>
                    </li>
                </ul>
            </div>
        </transition>
    </div>
</template>

<style scoped>
.slide-fade-enter-active, .slide-fade-leave-active {
    transition: opacity 0.5s ease, transform 0.5s ease;
}
.slide-fade-enter-from {
    opacity: 0;
    transform: translateY(-10px);
}
.slide-fade-leave-to {
    opacity: 0;
    transform: translateY(-10px);
}
</style>
