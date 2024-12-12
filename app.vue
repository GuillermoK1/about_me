<template>
  <div class="pt-2 w-dvh min-h-screen bg-slate-300 dark:bg-sky-900">
    <div class="m-2 flex justify-between">
      <h1 class="px-6 max-w-[50vw]">About project powered by NuxtUI and Tailwind.css</h1>
      <ColorScheme><USelect class="w-24 place-self-end" v-model="$colorMode.preference" :options="['system', 'light', 'dark']" /></ColorScheme>
    </div>
    <NuxtLayout class="w-[97vw] min-h-screen bg-inherit"/>
  </div>
</template>
