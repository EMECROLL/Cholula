<script setup lang="ts"></script>

<template>
  <div class="image-scroll-wrapper">
    <div class="image-scroll-container">
      <img src="../assets/Primera.jpg" alt="Primera imagen" />
      <img src="../assets/Segunda.jpg" alt="Segunda imagen" />
    </div>
  </div>
</template>

<style scoped>
.image-scroll-wrapper {
  margin-top: 20px;
  box-sizing: border-box;
  overflow-x: hidden;
}

.image-scroll-container {
  display: flex;
  flex-direction: row;
  overflow-x: auto;
  -ms-overflow-style: none;
  scrollbar-width: none;
}

.image-scroll-container::-webkit-scrollbar {
  display: none;
}

.image-scroll-container img {
  height: auto;
  width: auto;
  max-height: 680px;
  flex-shrink: 0;
}
</style>
