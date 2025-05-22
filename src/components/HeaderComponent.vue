<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <header class="bg-black text-white flex items-center justify-between px-8 py-4">
    <div class="flex items-center space-x-4">
      <img src="" alt="Pueblos Mágicos" class="w-10 h-10" />
      <span class="text-xl font-bold leading-tight tracking-wide">PUEBLOS<br />MÁGICOS</span>
    </div>

    <nav class="flex items-center space-x-8">
      <RouterLink to="/atractivos" class="hover:text-gray-300">Atractivos</RouterLink>
      <RouterLink to="/festividades" class="hover:text-gray-300">Festividades</RouterLink>
      <RouterLink to="/hoteles" class="hover:text-gray-300">Hoteles</RouterLink>
      <RouterLink to="/restaurantes" class="hover:text-gray-300">Restaurantes</RouterLink>
      <RouterLink to="/tours" class="hover:text-gray-300">Tours</RouterLink>

      <button aria-label="Buscar" class="hover:text-gray-300">
        LUPA
      </button>
    </nav>
  </header>
</template>
