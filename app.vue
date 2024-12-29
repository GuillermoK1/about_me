<script setup lang="ts">
useHead({
  htmlAttrs: { lang: 'es' },
  link: [{ rel: 'icon', href: '/faviconNuxt.ico' }]
})

useSeoMeta({
  viewport: 'width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no',
  title: 'About Guillermo Kabbabe',
  ogTitle: 'About Guillermo Kabbabe',
  description: 'About page, powered by NuxtUI and Tailwind.css.',
  ogDescription: 'About page, powered by NuxtUI and Tailwind.css.',
  ogImage: '/profile_picture.jpg',
  ogType: 'website',
  ogUrl: 'https://aboutme-ahl.pages.dev'
})
</script>

<template>
  <div class="pt-2 w-dvw min-h-screen bg-slate-300 dark:bg-sky-900">
    <div>
      <div class="m-2 flex">
        <ColorScheme><USelect class="w-24 mx-2 place-self-end overflow-visible" v-model="$colorMode.preference" :options="['system', 'light', 'dark']"/></ColorScheme>
        <h1 class="flex no-wrap"></h1>
          Project powered by
      </div>
      <div class="mx-2 flex">
        <img class="w-6 h-6 mx-2" src="/faviconNuxt.ico" alt="Nuxt logo"> 
          NuxtUI and
        <img class="w-6 h-6 mx-2" src="/faviconTailwind.png" alt="Tailwind logo"> 
          Tailwind.css
      </div>
    </div>
    <NuxtLayout class="w-full min-h-screen bg-inherit"/>
  </div>
</template>
