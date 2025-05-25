<script setup lang="ts">
import { RouterView } from 'vue-router'
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import 'primeicons/primeicons.css'
import '@fortawesome/fontawesome-free/css/all.min.css';

</script>

<template class="m-20">
  <HeaderComponent></HeaderComponent>
  <RouterView/>
  <FooterComponent></FooterComponent>
</template>
