<template>
  <div class="pt-2 w-dvw min-h-screen bg-slate-300 dark:bg-sky-900">
    <div class="m-2 flex justify-between">
      <h1 class="px-6 flex no-wrap">
        About project powered by   
        <img class="w-6 h-6 mx-2" src="/faviconNuxt.ico" alt="Nuxt logo"> 
         NuxtUI and   
        <img class="w-6 h-6 mx-2" src="/faviconTailwind.png" alt="Tailwind logo"> 
         Tailwind.css
      </h1>
      <ColorScheme><USelect class="w-24 place-self-end" v-model="$colorMode.preference" :options="['system', 'light', 'dark']" /></ColorScheme>
    </div>
    <NuxtLayout class="w-full min-h-screen bg-inherit"/>
  </div>
</template>
