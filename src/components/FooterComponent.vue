<script setup lang="ts">
import logo from '@/assets/Pueblos-Magicos-logo.png'

</script>

<style lang="css">

.contentinfo{
    display: flex;
    width: 100%;
    height: auto;
    justify-content: center;
    flex-direction: column;
    position: relative;
}

.iconslinefooter{
    position: absolute;
    top: 0;
    width: 100%;
    height: 2em;
    background: #FFF url(https://pueblosmagicos.mexicodesconocido.com.mx/wp-content/themes/pueblosmagicos/img/texture_icons2_alt.svg) repeat 50%;
    background-size: auto;
    z-index: 2;
}
</style>



<template>
  <footer role="contentinfo" class="bg-black text-gray-200">
    <div class="relative overflow-hidden">
      <div class="iconslinefooter"></div>
      <div class="flex flex-col justify-center items-center max-w-7xl mx-auto px-6 py-12 gap-2 md:gap-12">
        <div class="flex flex-col items-center space-y-6 my-10 gap-8">
          <img
            :src="logo"
            alt="Logo"
            width="250"
            class="max-w-full h-auto"
          />

          <div class="flex space-x-4 text-xl md:text-2xl gap-4 md:gap-8">
            <a
              href="https://www.facebook.com/mexicodesconocido"
              target="_blank"
              aria-label="Enlace al Facebook Oficial del sitio"
              class="socialbox fb hover:text-blue-600 transition-colors flex justify-center items-center"
              ><i class="pi pi-facebook text-2xl md:text-3xl"></i></a>
            <a
              href="https://twitter.com/mexdesconocido"
              target="_blank"
              aria-label="Enlace al Twitter Oficial del sitio"
              class="socialbox tw hover:text-blue-400 transition-colors flex justify-center items-center"
              ><i class="pi pi-twitter text-2xl md:text-3xl"></i
            ></a>
            <a
              href="https://www.instagram.com/mexicodesconocido/"
              target="_blank"
              aria-label="Enlace al Instagram Oficial del sitio"
              class="socialbox in hover:text-pink-500 transition-colors flex justify-center items-center"
              ><i class="pi pi-instagram text-2xl md:text-3xl"></i
            ></a>
            <a
              href="https://www.youtube.com/user/MEXICODESCONOCIDOTV"
              target="_blank"
              aria-label="Enlace al Youtube Oficial del sitio"
              class="socialbox yt hover:text-red-600 transition-colors flex justify-center items-center"
              ><i class="pi pi-youtube text-3xl md:text-4xl"></i
            ></a>
            <a
              href="https://www.tiktok.com/@mexicodesconocido"
              target="_blank"
              aria-label="Enlace al Tiktok Oficial del sitio"
              class="socialbox tk hover:text-cyan-400 transition-colors flex justify-center items-center"
              ><i class="pi pi-tiktok text-2xl md:text-3xl"></i
            ></a>
          </div>
        </div>

        <div class="w-full flex flex-col md:flex-row justify-around gap-8 nd:gap-0">
          <div>
            <h2 class="text-2xl font-semibold mb-3 text-center">Información</h2>
            <p class="flex flex-col justify-center">
              <a href="https://negocios.escapadas.mx/login?tab=signup/" target="_blank"
              class="hover:underline text-center text-lg"
                >Registro de Proveedores</a
              >
            </p>
          </div>

          <div>
            <h2 class="text-2xl font-semibold mb-3 text-center">Información</h2>
            <p class="flex flex-col justify-center">
              <a href="https://www.gob.mx/sectur" target="_blank" class="hover:underline text-center w-full text-lg">Secretaría de Turismo</a>
              <br />
              <a href="https://www.mexicodesconocido.com.mx/" target="_blank" class="hover:underline text-center text-lg">México Desconocido</a>
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="border-t border-[#e6007e] bg-[#e6007e] py-4">
    </div>
  </footer>
</template>
