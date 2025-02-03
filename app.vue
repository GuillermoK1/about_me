<script setup lang="ts">
useHead({
  htmlAttrs: { lang: 'es' },
  link: [
    { rel: 'icon', href: '/assets/favicon_128.ico' },
    { rel: 'canonical', href: 'https://www.gkdevservices.com' }],
  meta: [
    { name: 'robots', content: 'index, follow' },
    { name: 'author', content: 'gkdevservices.com' },
    { name: 'theme-color', content: '#6AA37F' }

  ]

})

useSeoMeta({
  viewport: 'width=device-width, initial-scale=1, maximum-scale=2.0',
  title: 'GK Dev Services',
  ogTitle: 'GK Dev Services',
  description: 'My website, powered by NuxtUI and Tailwind.css.',
  ogDescription: 'My website, powered by NuxtUI and Tailwind.css.',
  ogImage: '/assets/favicon.png',
  ogType: 'website',
  ogUrl: 'https://www.gkdevservices.com',
  ogSiteName: 'GK Dev Services',
  keywords: 'gkdevservices, gk, gkdev, devservices, Guillermo Kabbabe, My website, NuxtUI, Tailwind.css'
})
</script>

<template>
  <div class="pt-2 w-dvw min-h-screen bg-slate-300 dark:bg-sky-900">
    <div>
      <div class="m-2 flex">
        <h1 class="p-2 flex no-wrap rounded-l-lg bg-gradient-to-r from-gray-500/50 via-slate-500 to-emerald-500 text-emerald-400 font-bold">G</h1>
        <h1 class="p-2 flex no-wrap rounded-r-lg bg-gradient-to-r from-emerald-500 via-slate-500 to-gray-500/50 text-slate-300 font-bold">K</h1>
        <ColorScheme><USelect class="w-24 mx-2 place-self-end overflow-visible" v-model="$colorMode.preference" :options="['system', 'light', 'dark']"/></ColorScheme>
        <h1 class="m-2 p-2 flex no-wrap"></h1>
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
