<script setup lang="ts">
import { ref, onMounted } from 'vue'

interface ProjectItem {
  src: string
  link: string
  title: string
  description: string
  tech: string[]
}

const items: ProjectItem[] = [
  {
    src: 'assets/plasmap/plasmap-thumbnail.png',
    link: '/plasmap',
    title: 'PLASMAP Platform',
    description: 'Enterprise-grade service discovery platform for provincial networks',
    tech: ['Nuxt 3', 'TypeScript', 'Others']
  },
  {
    src: 'assets/Python/readme_capture.png',
    link: '/python',
    title: 'Python Analytics',
    description: 'Data analysis and visualization tools',
    tech: ['Python', 'Pandas', 'NumPy']
  },
  {
    src: 'assets/themes/themes_capture.png',
    link: '/themes',
    title: 'Theme Builder',
    description: 'Custom theming system for web applications',
    tech: ['NuxtUI', 'Tailwindcss', 'TypeScript']
  },
  {
    src: 'assets/capture-new-project.png',
    link: '/new',
    title: 'Project Template',
    description: 'Modern web development starter template',
    tech: ['NuxtUI', 'TypeScript', 'Tailwindcss']
  }
]

</script>

<template>
  <div class="max-w-7xl mx-auto px-4 py-12">
    <h1 class="text-4xl font-bold text-center mb-8">Featured Projects</h1>
    <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
      <NuxtLink
        v-for="item in items"
        :key="item.title"
        :to="item.link"
        class="group pb-2 rounded border shadow-lg hover:shadow-xl transition-all duration-300"
      >
        <div class="grid place-items-center rounded">
          <img
            :src="item.src"
            :alt="`${item.title} thumbnail`"
            class="w-auto h-auto rounded transition-transform duration-300 group-hover:scale-105"
          >
        </div>
        <div class="group p-4">
          <h3 class="font-semibold text-lg mb-2">{{ item.title }}</h3>
          <p class="text-gray-600 dark:text-gray-300 text-sm">{{ item.description }}</p>
        </div>
        <span 
          v-for="tech in item.tech" 
          :key="tech"
          class="m-1 px-3 py-1 rounded-full bg-white/20 text-sm text-white dark:text-black"
        >
          {{ tech }}
        </span>
      </NuxtLink>
    </div>
  </div>
</template>
