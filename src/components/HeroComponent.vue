<template>
    <section class="hero p-30 space-y-8">
        <h1 class="text-white text-7xl font-extrabold mb-5">Cholula</h1>
        <h2 class="text-white text-5xl font-bold">Puebla</h2>
        <hr class="w-[60%] text-white border-[1.5px]">
        <p class="text-white text-xl tracking-wide">Como queriendo alcanzar a ese gigante nevado, <br>se eleva el Santuario de Nuestra Señora de los Remedios, <br>la
            iglesia de cúpulas cubiertas de azulejos que los españoles <br>edificaron en el siglo XVI, encima de la Gran
            Pirámide.</p>
        <button class="btn">Vive su magia</button>
    </section>
</template>

<style scoped>
.hero {
    background: rgba(0, 0, 0, 0.3) url("/src/assets/images/cholula_hero.jpg");
    background-blend-mode: darken;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: start;
    text-align: start;
}

.btn{
    background-color: #e6007e;
    color: white;
    padding: 6px 32px;
    border-radius: 10px;
    font-weight: 600;
    cursor: pointer;
    transition: all;
    transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.btn:hover{
    transform: scale(1.1);
    transition: 0.3s;
}

.btn:active{
    background-color: #a61263;
}
</style>