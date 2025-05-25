<template>
    <div class="max-w-7xl mx-auto px-4 py-8 pt-25">
        <!-- Título principal -->
        <h1 class="text-5xl font-bold mb-12">Vive su magia</h1>

        <!-- Sección principal con flex para mejor control del espaciado -->
        <div class="flex flex-col lg:flex-row gap-14 mb-12">
            <!-- Columna izquierda - Contenido principal -->
            <div class="flex-1 lg:flex-[2] space-y-8">
                <!-- Descripción principal -->
                <div class="text-base leading-relaxed">
                    <p>
                        A la urbe de los dos pueblos, el de San Pedro y San Andrés, la acompaña
                        el volcán Popocatépetl. Como queriendo alcanzar a ese gigante nevado,
                        se eleva el Santuario de Nuestra Señora de los Remedios, la iglesia de
                        cúpulas cubiertas de azulejos que los españoles edificaron en el siglo XVI.
                        La colocaron justo encima de la Gran Pirámide, el basamento que más
                        parece cerro que sitio arqueológico. Debajo van y vienen los días, la gente,
                        la vida.
                    </p>
                </div>

                <!-- Sección El motivo -->
                <div>
                    <h2 class="text-3xl font-bold mb-6">El motivo</h2>
                    <div class="space-y-4">
                        <p class="text-base font-medium mb-2">La pirámide con una iglesia encima:</p>
                        <div class="space-y-1 text-base">
                            <p>
                                <span class="font-semibold">1.</span> La Gran Pirámide de Cholula mide 60 metros de
                                altura y 400 metros por lado.
                            </p>
                            <p>
                                <span class="font-semibold">2.</span> Es uno de los basamentos piramidales más grandes
                                del mundo y está hecho de estructuras superpuestas.
                            </p>
                            <p>
                                <span class="font-semibold">3.</span> El museo de sitio, un túnel al interior de la
                                pirámide de 280 metros y dos patios ceremoniales pueden ser visitados.
                            </p>
                            <p>
                                <span class="font-semibold">4.</span> En su cúspide levantaron los franciscanos el
                                Santuario de Nuestra Señora de los Remedios.
                            </p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Columna derecha - Mapa con mejor manejo de imagen -->
            <div class="flex-1 lg:max-w-sm ml-4">
                <div class="bg-gray-100 rounded-lg overflow-hidden shadow-md ">
                    <img
                        src="/src/assets/MapaCholula.png"
                        alt="Mapa de Cholula"
                        class="w-full h-96 object-cover
"
                    />
                </div>
            </div>
        </div>

        <!-- Sección Lo básico -->
        <div class="mb-8">
            <h2 class="text-3xl font-bold mb-6">Lo básico</h2>
            <div class="text-base leading-relaxed">
                <p>
                    Admira las pinturas murales que hay en la pirámide, como las de Los Bebedores y Los Chapulines.
                </p>
            </div>
        </div>

        <!-- Sección Imprescindibles -->
        <div class="mb-8">
            <h2 class="text-3xl font-bold mb-6">Imprescindibles</h2>
            <div class="text-base leading-relaxed space-y-1">
                <p>
                    <span class="font-semibold">1.</span>
                    Subir al Santuario de Nuestra Señora de los Remedios para admirar la ciudad y el volcán Popocatépetl.
                </p>
                <p>
                    <span class="font-semibold">2.</span>
                    Conocer las plazas principales tanto de San Pedro como San Andrés, los pueblos hermanos.
                </p>
                <p>
                    <span class="font-semibold">3.</span>
                    Saborear cualquier postre del Café Ocho 30, en San Andrés.
                </p>
            </div>
        </div>
    </div>
</template>
