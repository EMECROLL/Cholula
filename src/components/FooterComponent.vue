<script setup lang="ts">
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
    <div class="iconslinefooter"></div>

    <div class="relative overflow-hidden">
      <div class="relative max-w-7xl mx-auto px-6 py-12 grid gap-12 md:grid-cols-2 lg:grid-cols-3">
        <div class="flex flex-col items-start space-y-6">
          <img
            src="https://pueblosmag2023.wpengine.com/wp-content/uploads/2023/09/pm_md-1.svg"
            alt="Logo"
            width="360"
            height="61"
            class="max-w-full h-auto"
          />

          <div class="flex space-x-4 text-2xl">
            <a
              href="https://www.facebook.com/mexicodesconocido"
              target="_blank"
              aria-label="Enlace al Facebook Oficial del sitio"
              class="socialbox fb hover:text-blue-600 transition-colors"
              ><i class="fa-brands fa-facebook-f"></i
            ></a>
            <a
              href="https://twitter.com/mexdesconocido"
              target="_blank"
              aria-label="Enlace al Twitter Oficial del sitio"
              class="socialbox tw hover:text-blue-400 transition-colors"
              ><i class="fa-brands fa-twitter"></i
            ></a>
            <a
              href="https://www.instagram.com/mexicodesconocido/"
              target="_blank"
              aria-label="Enlace al Instagram Oficial del sitio"
              class="socialbox in hover:text-pink-500 transition-colors"
              ><i class="fa-brands fa-instagram"></i
            ></a>
            <a
              href="https://www.youtube.com/user/MEXICODESCONOCIDOTV"
              target="_blank"
              aria-label="Enlace al Youtube Oficial del sitio"
              class="socialbox yt hover:text-red-600 transition-colors"
              ><i class="fa-brands fa-youtube"></i
            ></a>
            <a
              href="https://www.tiktok.com/@mexicodesconocido"
              target="_blank"
              aria-label="Enlace al Tiktok Oficial del sitio"
              class="socialbox tk hover:text-black transition-colors"
              ><i class="fa-brands fa-tiktok"></i
            ></a>
          </div>
        </div>

        <div class="w-full flex justify-between">
          <div class="flex justify-center items-center">
          </div>

          <div>
            <h2 class="text-xl font-semibold mb-3">Información</h2>
            <p>
              <a href="https://negocios.escapadas.mx/login?tab=signup/" class="hover:underline"
                >Registro de Proveedores</a
              >
            </p>
          </div>

          <div>
            <h2 class="text-xl font-semibold mb-3">Información</h2>
            <p>
              <a href="https://www.gob.mx/sectur" class="hover:underline">Secretaría de Turismo</a><br />
              <a href="https://www.mexicodesconocido.com.mx/" class="hover:underline">México Desconocido</a>
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="border-t border-[#e6007e] bg-[#e6007e] py-4">
    </div>
  </footer>
</template>
