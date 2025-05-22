<script setup lang="ts">
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
  <div class="w-full bg-gray-50 py-8">
    <!-- Header con información del clima -->
    <div class="max-w-6xl mx-auto px-4 mb-8">
      <div class="flex justify-between items-start">
        <div class="flex-1">
          <h2 class="text-2xl font-bold text-gray-800 mb-2">
            {{ props.description }}
          </h2>
        </div>
        
        <div class="text-right">
          <h3 class="text-xl font-semibold text-gray-700 mb-2">{{ props.location }}</h3>
          <div class="flex items-center justify-end space-x-4">
            <div class="flex items-center">
              <i class="pi pi-cloud text-2xl text-gray-600 mr-2"></i>
              <span class="text-lg">Lluvia ligera</span>
            </div>
            <div class="text-3xl font-bold">{{ props.temperature }}°</div>
            <div class="text-lg">
              <span class="text-gray-600">Porcentaje humedad</span>
              <div class="font-bold">{{ props.humidity }}%</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Secciones coloridas -->
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex gap-0 rounded-lg overflow-hidden shadow-lg justify-center">
        <!-- Atractivos -->
        <div class="bg-green-500 text-white p-8 text-center relative flex flex-col justify-between" style="width: 290px; height: 455px;">
          <h3 class="text-xl font-bold mb-4">Atractivos</h3>
          <div class="flex-1 flex items-center justify-center">
            <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center">
              <i class="pi pi-camera text-2xl"></i>
            </div>
          </div>
        </div>

        <!-- Festividades -->
        <div class="bg-orange-500 text-white p-8 text-center relative flex flex-col justify-between" style="width: 290px; height: 455px;">
          <h3 class="text-xl font-bold mb-4">Festividades</h3>
          <div class="flex-1 flex items-center justify-center">
            <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center">
              <i class="pi pi-calendar text-2xl"></i>
            </div>
          </div>
        </div>

        <!-- Hoteles -->
        <div class="bg-pink-500 text-white p-8 text-center relative flex flex-col justify-between" style="width: 290px; height: 455px;">
          <h3 class="text-xl font-bold mb-4">Hoteles</h3>
          <div class="flex-1 flex items-center justify-center">
            <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center">
              <i class="pi pi-home text-2xl"></i>
            </div>
          </div>
        </div>

        <!-- Restaurantes -->
        <div class="bg-purple-600 text-white p-8 text-center relative flex flex-col justify-between" style="width: 290px; height: 455px;">
          <h3 class="text-xl font-bold mb-4">Restaurantes</h3>
          <div class="flex-1 flex items-center justify-center">
            <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center">
              <i class="pi pi-shopping-bag text-2xl"></i>
            </div>
          </div>
        </div>

        <!-- Tours -->
        <div class="bg-cyan-500 text-white p-8 text-center relative flex flex-col justify-between" style="width: 290px; height: 455px;">
          <h3 class="text-xl font-bold mb-4">Tours</h3>
          <div class="flex-1 flex items-center justify-center">
            <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center">
              <i class="pi pi-map text-2xl"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

