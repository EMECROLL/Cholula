<script setup lang="ts">
import imgAtractivos from '@/assets/images/imgAtractivos.png'
import imgFestividades from '@/assets/images/imgFestividades.png'
import imgHoteles from '@/assets/images/imgHoteles.png'
import imgRestaurantes from '@/assets/images/imgRestaurantes.png'
import imgTours from '@/assets/images/imgTours.png'
import { ref, onMounted } from 'vue'

// Props opcionales para personalizar el componente
interface Props {
  description?: string
  location?: string
}

const props = withDefaults(defineProps<Props>(), {
  description: '"La ciudad de los que huyeron donde está el cerro hecho a mano".',
  location: 'Clima actual',
})

const temperature = ref<number>(18)
const humidity = ref<number>(80)
const weatherDescription = ref<string>('Lluvia ligera')

onMounted(async () => {
  try {
    const lat = 19.0622
    const lon = -98.303
    const apiKey = '33e0d3a5b1b105ad07365c815845d68d'

    const response = await fetch(
      `https://api.openweathermap.org/data/2.5/weather?lat=${lat}&lon=${lon}&appid=${apiKey}&units=metric&lang=es`,
    )

    const data = await response.json()

    if (data.main?.temp != null) temperature.value = Math.round(data.main.temp)
    if (data.main?.humidity != null) humidity.value = data.main.humidity
    if (data.weather && data.weather.length > 0 && data.weather[0].description) {
      weatherDescription.value = data.weather[0].description // actualizar descripción
    }
  } catch (error) {
    console.error('Error al obtener datos del clima:', error)
  }
})
console.log(weatherDescription)
</script>

<template>
  <div class="w-full">
    <!-- Header con información del clima -->
    <div class="w-full flex justify-center px-4">
      <div class="flex flex-col lg:flex-row w-full max-w-[1455px]">
        <!-- Div izquierdo - Descripción -->
        <div class="bg-white flex items-center p-4 lg:p-8" style="flex: 1">
          <h2 class="text-xl sm:text-2xl lg:text-4xl font-bold text-center lg:text-left">
            {{ props.description }}
          </h2>
        </div>
        <!-- Div derecho - Clima -->
        <div
          class="bg-white flex items-center justify-center lg:justify-end p-4 lg:p-8 min-h-[200px] lg:h-[355px]"
          style="flex: 1"
        >
          <div class="text-center lg:text-right w-full">
            <h3 class="text-3xl sm:text-3xl lg:text-4xl font-bold text-scenter lg:text-left mb-4">
              {{ props.location }}
            </h3>
            <div
              class="flex flex-col sm:flex-row items-center justify-center lg:justify-end space-y-4 sm:space-y-0 sm:space-x-6"
            >
              <div
                class="flex flex-row flex-wrap items-center justify-center lg:justify-start gap-x-3 w-full mt-4"
              >
                <div class="flex justify-center lg:justify-start">
                  <i class="pi pi-cloud text-4xl sm:text-5xl lg:text-6xl"></i>
                </div>
                <div class="flex items-center">
                  <span class="text-lg sm:text-xl lg:text-2xl font-bold">
                    {{ weatherDescription }}
                  </span>
                </div>
                <div class="text-3xl sm:text-4xl lg:text-5xl font-bold">
                  {{ temperature !== null ? temperature + '°' : '...' }}
                </div>
              </div>
              <div class="text-3xl sm:text-lg lg:text-xl">
                <div class="flex items-center gap-x-2">
                  <span class="text-lg sm:text-xl lg:text-2xl font-bold">Porcentaje humedad</span>
                  <div class="text-3xl sm:text-4xl lg:text-5xl font-bold">
                    {{ humidity !== null ? humidity + '%' : '...' }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Secciones coloridas -->
    <div class="w-full flex justify-center px-4 mt-5">
      <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-5 gap-0 overflow-hidden shadow-lg w-full max-w-[1455px]"
      >
        <!-- Atractivos -->
        <div
          class="text-white p-4 sm:p-6 lg:p-8 text-center relative flex flex-col justify-between h-[300px] sm:h-[400px] lg:h-[455px]"
          style="background-color: #3aa438"
        >
          <h3 class="text-lg sm:text-xl lg:text-2xl font-bold mt-[30px] sm:mt-[45px] lg:mt-[60px]">
            Atractivos
          </h3>
          <div class="flex-1 flex items-center justify-center">
            <img
              :src="imgAtractivos"
              alt="Atractivos"
              class="w-[120px] h-[148px] sm:w-[140px] sm:h-[173px] lg:w-[160px] lg:h-[198px] object-contain"
            />
          </div>
        </div>

        <!-- Festividades -->
        <div
          class="text-white p-4 sm:p-6 lg:p-8 text-center relative flex flex-col justify-between h-[300px] sm:h-[400px] lg:h-[455px]"
          style="background-color: #e64e23"
        >
          <h3 class="text-lg sm:text-xl lg:text-2xl font-bold mt-[30px] sm:mt-[45px] lg:mt-[60px]">
            Festividades
          </h3>
          <div class="flex-1 flex items-center justify-center">
            <img
              :src="imgFestividades"
              alt="Festividades"
              class="w-[120px] h-[148px] sm:w-[140px] sm:h-[173px] lg:w-[160px] lg:h-[198px] object-contain"
            />
          </div>
        </div>

        <!-- Hoteles -->
        <div
          class="text-white p-4 sm:p-6 lg:p-8 text-center relative flex flex-col justify-between h-[300px] sm:h-[400px] lg:h-[455px]"
          style="background-color: #e6007e"
        >
          <h3 class="text-lg sm:text-xl lg:text-2xl font-bold mt-[30px] sm:mt-[45px] lg:mt-[60px]">
            Hoteles
          </h3>
          <div class="flex-1 flex items-center justify-center">
            <img
              :src="imgHoteles"
              alt="Hoteles"
              class="w-[120px] h-[148px] sm:w-[140px] sm:h-[173px] lg:w-[160px] lg:h-[198px] object-contain"
            />
          </div>
        </div>

        <!-- Restaurantes -->
        <div
          class="text-white p-4 sm:p-6 lg:p-8 text-center relative flex flex-col justify-between h-[300px] sm:h-[400px] lg:h-[455px]"
          style="background-color: #743b8d"
        >
          <h3 class="text-lg sm:text-xl lg:text-2xl font-bold mt-[30px] sm:mt-[45px] lg:mt-[60px]">
            Restaurantes
          </h3>
          <div class="flex-1 flex items-center justify-center">
            <img
              :src="imgRestaurantes"
              alt="Restaurantes"
              class="w-[120px] h-[148px] sm:w-[140px] sm:h-[173px] lg:w-[160px] lg:h-[198px] object-contain"
            />
          </div>
        </div>

        <!-- Tours -->
        <div
          class="text-white p-4 sm:p-6 lg:p-8 text-center relative flex flex-col justify-between h-[300px] sm:h-[400px] lg:h-[455px]"
          style="background-color: #00a4dd"
        >
          <h3 class="text-lg sm:text-xl lg:text-2xl font-bold mt-[30px] sm:mt-[45px] lg:mt-[60px]">
            Tours
          </h3>
          <div class="flex-1 flex items-center justify-center">
            <img
              :src="imgTours"
              alt="Tours"
              class="w-[120px] h-[148px] sm:w-[140px] sm:h-[173px] lg:w-[160px] lg:h-[198px] object-contain"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
