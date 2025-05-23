<script setup lang="ts">
import { RouterLink } from 'vue-router'
import logo from '@/assets/Pueblos-Magicos-logo.png'

</script>

<template>
  <header class="bg-black text-white flex items-center justify-around py-4">
    <div class="flex items-center space-x-4">
      <img :src="logo" alt="Pueblos Mágicos" class="h-15" />
    </div>

    <nav class="flex items-center space-x-15 p-8">
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Atractivos</RouterLink>
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Festividades</RouterLink>
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Hoteles</RouterLink>
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Restaurantes</RouterLink>
      <RouterLink to="/" class="hover:text-gray-300 text-lg">Tours</RouterLink>

      <button aria-label="Buscar" class="hover:text-gray-300">
        <i class="pi pi-search"></i>
      </button>
    </nav>
  </header>
</template>
