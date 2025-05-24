<script setup lang="ts">
import { ref } from 'vue'
import { RouterLink } from 'vue-router'
import logo from '@/assets/Pueblos-Magicos-logo.png'

const isMenuOpen = ref(false)
</script>

<template>
  <header class="bg-black text-white flex flex-wrap items-center justify-between md:justify-around p-4">
    <div class="flex items-center space-x-4">
      <img :src="logo" alt="Pueblos Mágicos" class="h-12 md:h-[60px]" />
    </div>

    <div class="flex gap-4">
      <button aria-label="Buscar" class="md:hidden hover:text-gray-300">
        <i class="pi pi-search text-lg"></i>
      </button>
      <button
      @click="isMenuOpen = !isMenuOpen"
      class="md:hidden text-white"
      aria-label="Toggle menu">
        <i class="pi pi-bars text-2xl"></i>
      </button>
    </div>


    <nav class="hidden md:flex items-center space-x-[60px] p-8">
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Atractivos</RouterLink>
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Festividades</RouterLink>
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Hoteles</RouterLink>
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Restaurantes</RouterLink>
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Tours</RouterLink>

      <button aria-label="Buscar" class="hover:text-gray-300 cursor-pointer">
        <i class="pi pi-search text-lg"></i>
      </button>
    </nav>

      <nav v-if="isMenuOpen" class="w-full flex flex-col items-start space-y-4 mt-4 md:hidden">
        <RouterLink to="/" class="hover:text-gray-300 text-lg w-full">Atractivos</RouterLink>
        <RouterLink to="/" class="hover:text-gray-300 text-lg w-full">Festividades</RouterLink>
        <RouterLink to="/" class="hover:text-gray-300 text-lg w-full">Hoteles</RouterLink>
        <RouterLink to="/" class="hover:text-gray-300 text-lg w-full">Restaurantes</RouterLink>
        <RouterLink to="/" class="hover:text-gray-300 text-lg w-full">Tours</RouterLink>
      </nav>

  </header>
</template>
