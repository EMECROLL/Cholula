<script setup lang="ts">
import imgAtractivos from '@/assets/images/imgAtractivos.png'
import imgFestividades from '@/assets/images/imgFestividades.png'
import imgHoteles from '@/assets/images/imgHoteles.png'
import imgRestaurantes from '@/assets/images/imgRestaurantes.png'
import imgTours from '@/assets/images/imgTours.png'

// Props opcionales para personalizar el componente
interface Props {
  temperature?: number
  humidity?: number
  description?: string
  location?: string
}

const props = withDefaults(defineProps<Props>(), {
  temperature: 18,
  humidity: 80,
  description: '"La ciudad de los que huyeron donde está el cerro hecho a mano".',
  location: 'Clima actual'
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
              <div class="text-5xl font-bold">{{ props.temperature }}°</div>
              <div class="text-xl">
                <span class="text-gray-600">Porcentaje humedad</span>
                <div class="font-bold text-2xl">{{ props.humidity }}%</div>
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