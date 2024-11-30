<template>
  <div class="p-8 w-dvw h-dvh bg-slate-300 dark:bg-slate-900">
    <div class="m-2 flex justify-between">
      <h1>About page powered by NuxtUI and Tailwind.css</h1>
      <ColorScheme><USelect class="w-24 place-self-end" v-model="$colorMode.preference" :options="['system', 'light', 'dark']" /></ColorScheme>
    </div>
    <NuxtLayout/>
  </div>
</template>
