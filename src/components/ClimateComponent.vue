<script setup lang="ts">
import imgAtractivos from '@/assets/images/imgAtractivos.png'
import imgFestividades from '@/assets/images/imgFestividades.png'
import imgHoteles from '@/assets/images/imgHoteles.png'
import imgRestaurantes from '@/assets/images/imgRestaurantes.png'
import imgTours from '@/assets/images/imgTours.png'

// Props opcionales para personalizar el componente
interface Props {
  description?: string
  location?: string
}

const props = withDefaults(defineProps<Props>(), {
  description: '"La ciudad de los que huyeron donde está el cerro hecho a mano".',
  location: 'Clima actual'
})

import { ref, onMounted } from 'vue'

const temperature = ref<number>(18)
const humidity = ref<number>(80)
onMounted(async () => {
  try {
    const lat = 19.0622
    const lon = -98.3030
    const apiKey = '33e0d3a5b1b105ad07365c815845d68d'

    const response = await fetch(
      `https://api.openweathermap.org/data/2.5/weather?lat=${lat}&lon=${lon}&appid=${apiKey}&units=metric&lang=es`
    )

    const data = await response.json()

    if (data.main?.temp != null) temperature.value = Math.round(data.main.temp)
    if (data.main?.humidity != null) humidity.value = data.main.humidity
  } catch (error) {
    console.error('Error al obtener datos del clima:', error)
  }
})

</script>


<template>
  <div class="w-full bg-gray-50">
    <!-- Header con información del clima -->
    <div class="w-full flex justify-center">
      <div class="flex" style="width: 1455px;">
        <!-- Div izquierdo - Descripción -->
        <div class="bg-white flex items-center" style="flex: 1;">
          <h2 class="text-4xl font-bold">
            {{ props.description }}
          </h2>
        </div>

<!-- Div derecho - Clima -->
<div class="bg-white flex items-center justify-end" style="flex: 1; height: 355px;">
  <div class="text-right">
    <h3 class="text-2xl font-semibold text-gray-700 mb-2">{{ props.location }}</h3>
    <div class="flex items-center justify-end space-x-6">
      <div class="flex items-center">
        <i class="pi pi-cloud text-4xl mr-3"></i>
        <span class="text-2xl font-bold">Lluvia ligera</span>
      </div>
      <div class="text-5xl font-bold">
        {{ temperature !== null ? temperature + '°' : '...' }}
      </div>
      <div class="text-xl">
        <span class="text-gray-600">Porcentaje humedad</span>
        <div class="font-bold text-2xl">
          {{ humidity !== null ? humidity + '%' : '...' }}
        </div>
      </div>
    </div>
  </div>
</div>

      </div>
    </div>

    <!-- Secciones coloridas -->
    <div class="w-full flex justify-center">
      <div class="flex gap-0 overflow-hidden shadow-lg" style="width: 1455px;">
        <!-- Atractivos -->
        <div class="text-white p-8 text-center relative flex flex-col justify-between" style="width: 291px; height: 455px; background-color: #3aa438;">
          <h3 class="text-2xl font-bold mt-[60px]">Atractivos</h3>
          <div class="flex-1 flex items-center justify-center">
            <img :src="imgAtractivos" alt="Atractivos" class="w-[160px] h-[198px] object-contain" />
          </div>
        </div>

        <!-- Festividades -->
        <div class="text-white p-8 text-center relative flex flex-col justify-between" style="width: 291px; height: 455px; background-color: #e64e23;">
          <h3 class="text-2xl font-bold mt-[60px]">Festividades</h3>
          <div class="flex-1 flex items-center justify-center">
            <img :src="imgFestividades" alt="Festividades" class="w-[160px] h-[198px] object-contain" />
          </div>
        </div>

        <!-- Hoteles -->
        <div class="text-white p-8 text-center relative flex flex-col justify-between" style="width: 291px; height: 455px; background-color: #e6007e;">
          <h3 class="text-2xl font-bold mt-[60px]">Hoteles</h3>
          <div class="flex-1 flex items-center justify-center">
            <img :src="imgHoteles" alt="Hoteles" class="w-[160px] h-[198px] object-contain" />
          </div>
        </div>

        <!-- Restaurantes -->
        <div class="text-white p-8 text-center relative flex flex-col justify-between" style="width: 291px; height: 455px; background-color: #743b8d;">
          <h3 class="text-2xl font-bold mt-[60px]">Restaurantes</h3>
          <div class="flex-1 flex items-center justify-center">
            <img :src="imgRestaurantes" alt="Restaurantes" class="w-[160px] h-[198px] object-contain" />
          </div>
        </div>

        <!-- Tours -->
        <div class="text-white p-8 text-center relative flex flex-col justify-between" style="width: 291px; height: 455px; background-color: #00a4dd;">
          <h3 class="text-2xl font-bold mt-[60px]">Tours</h3>
          <div class="flex-1 flex items-center justify-center">
            <img :src="imgTours" alt="Tours" class="w-[160px] h-[198px] object-contain" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
