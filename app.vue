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
  ogImage: '/assets/favicon_upscaled.png',
  ogType: 'website',
  ogUrl: 'https://www.gkdevservices.com',
  ogSiteName: 'GK Dev Services',
  keywords: 'gkdevservices, gk, gkdev, devservices, Guillermo Kabbabe, My website, NuxtUI, Tailwind.css'
})

const colorMode = useColorMode()

// Initialize color mode preference
onMounted(() => {
  // Set initial color mode based on system preference
  if (!colorMode.preference) {
    colorMode.preference = window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light'
  }
})

const toggleColorMode = () => {
  colorMode.preference = colorMode.preference === 'dark' ? 'light' : 'dark'
}

</script>

<template>
  <div class="pt-2 w-dvw min-h-screen bg-slate-300 dark:bg-sky-900">
    <div class="mx-2 flex">
      <img class="w-6 h-6 mx-2" src="/faviconNuxt.ico" alt="Nuxt logo" /> 
        NuxtUI and
      <img class="w-6 h-6 mx-2" src="/faviconTailwind.png" alt="Tailwind logo" /> 
        Tailwind.css
    </div>
    <div class="mx-4 flex">
      <h1 class="p-2 font-bold text-2xl flex no-wrap bg-gradient-to-r from-gray-400 via-emerald-500 to-gray-400 bg-clip-text text-transparent hover:from-emerald-500 hover:via-gray-500 hover:to-emerald-500 transition-all duration-300">GKDevServices.com</h1>
      <ClientOnly>
        <UButton
        class="mx-2 w-10 h-10 ml-8"
        variant="ghost"
        color="black"
        :icon="colorMode.value === 'dark' ? 'i-heroicons-moon' : 'i-heroicons-sun'"
        @click="toggleColorMode"
      />
      </ClientOnly>
    </div>
    <NuxtLayout class="w-full min-h-max bg-inherit"/>
  </div>
</template>
