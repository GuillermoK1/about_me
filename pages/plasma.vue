<script setup lang="ts">
import { ref, onMounted } from 'vue'

const items = [ // Imágenes servidas localmente en la carpeta ~public.
  { src: 'assets/plasma/capture_plasma_pages_login.jpg' },
  { src: 'assets/plasma/capture_plasma_pages_logged.jpg' },
  { src: 'assets/plasma/capture_plasmas_pages_register.jpg' },
]

const carouselRef = ref()

onMounted(() => {
  setInterval(() => {
    if (!carouselRef.value) return

    if (carouselRef.value.page === carouselRef.value.pages) {
      return carouselRef.value.select(0)
    }

    carouselRef.value.next()
  }, 3000)
})
</script>

<template>
    <section class="p-4">
        <h1>PLASMA, rápido y seguro. </h1>
        <p class="text-sky-500 "><a href="https://plasma.nuxt.dev">Visitar el sitio </a></p>
        <h2>
            Plataforma de Servicios Múltiples Adaptables
        </h2>
        <h3>
            Algo más que una bolsa de empleo. Ofrece tus servicios, o busca trabajadores y empresas que ofrecen sus servicios.
            Usando esta plataforma ayudas a reducir el tráfico en las carreteras y autpoistas debido a que los resultados de búsqueda se ordenan por distancia.
            Reduciendo el tráfico pones tu granito de arena a favor de reducir las emisiones de gases contaminantes y el estrés en carretera.
            ¿Te imaginas una empresa donde sus empleados viven muy cerca? ¿Te imaginas llamar a una empresa de cerrajería por una emergencia y vengan en seguida porque se ubican cerca de tu hogar?
            Si estás en contra de escuchar lo típico: "El profesional que lo atenderá se encuentra realizando otro trabajo a 80 kilómetros de aquí, pero no se preocupe que vendrá en seguida" - si no pilla tráfico claro -.
        </h3>
        <UCarousel
        ref="carouselRef"
        v-slot="{ item }"
        :items="items"
        :ui="{ item: 'basis-full' }"
        class="m-2 max-w-64 rounded-lg overflow-hidden object-scale-down"
        indicators
        arrows
        >
        <a>
        <img :src="item.src" class="w-full" draggable="false" alt="Oops! Failed to load image...">
        </a>
        </UCarousel>
    </section>
</template>
