<script setup lang="ts">
import { ref, onMounted } from 'vue'

const items = [
  { src: 'https://picsum.photos/1920/1080?random=1', link: '/plasma' },
  { src: 'https://picsum.photos/1920/1080?random=2', link: '/page2' },
  { src: 'https://picsum.photos/1920/1080?random=3', link: '/page3' },
  { src: 'https://picsum.photos/1920/1080?random=4', link: '/page4' },
  { src: 'https://picsum.photos/1920/1080?random=5', link: '/page5' },
  { src: 'https://picsum.photos/1920/1080?random=6', link: '/page6' },
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
  <UCarousel
    ref="carouselRef"
    v-slot="{ item }"
    :items="items"
    :ui="{ item: 'basis-full' }"
    class="rounded-lg overflow-hidden"
    indicators
    arrows
  >
    <a :href="item.link">
      <img :src="item.src" class="w-full" draggable="false" alt="Oops! Failed to load image...">
    </a>
  </UCarousel>
</template>
