<script setup lang="ts">
import { ref, onMounted } from 'vue'

const items = [ // Imágenes servidas localmente en la carpeta ~public.
  { src: 'assets/plasma/circulo.jpg', link: '/plasma' },
  { src: 'assets/Python/readme_capture.png', link: '/python' },
  { src: 'assets/themes/capture_color_pallets_tailwind.png', link: '/themes' },
  { src: 'assets/capture-new-project.png', link: '/new' },

]

const carouselRef = ref()

onMounted(() => {
  setInterval(() => {
    if (!carouselRef.value) return

    if (carouselRef.value.page === carouselRef.value.pages) {
      return carouselRef.value.select(0)
    }

    carouselRef.value.next()
  }, 5000)
})
</script>

<template>
    <UCarousel
      ref="carouselRef"
      v-slot="{ item }"
      :items="items"
      :ui="{ item: 'basis-full' }"
      class="rounded-lg overflow-hidden h-fit flex"
      indicators
      arrows
    >
      <a :href="item.link">
        <img :src="item.src" class="w-full grow" draggable="false" alt="Oops! Failed to load image...">
      </a>
    </UCarousel>
</template>
