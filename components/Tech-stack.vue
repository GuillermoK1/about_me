<template>
  <div class="w-auto p-6 bg-gray-50 dark:bg-gray-800 rounded-lg shadow-lg">
    <div class="w-auto grid grid-cols-2 gap-8">
      <!-- Familiar Technologies -->
      <div class="tech-section">
        <h3 class="text-xl font-bold mb-4 text-indigo-600 dark:text-indigo-400">
          Familiar Technologies
        </h3>
        <div class="flex flex-wrap gap-2">
          <span v-for="tech in familiarTech" :key="tech"
            class="px-3 py-1 bg-indigo-100 dark:bg-indigo-900 rounded-full text-indigo-700 dark:text-indigo-300 text-sm">
            {{ tech }}
          </span>
        </div>
      </div>

      <!-- Current Stack -->
      <div class="tech-section">
        <h3 class="text-xl font-bold mb-4 text-emerald-600 dark:text-emerald-400">
          Current Stack
        </h3>
        <div class="flex flex-wrap gap-2">
          <span v-for="tech in currentStack" :key="tech"
            class="px-3 py-1 bg-emerald-100 dark:bg-emerald-900 rounded-full text-emerald-700 dark:text-emerald-300 text-sm">
            {{ tech }}
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const familiarTech = [
  'Python',
  'Pandas',
  'Numpy',
  'Matplotlib',
  'Javascript',
  'Vue',
  'Google C. P.',
  'Wordpress',
  'Shopify'
]

const currentStack = [
  'Typescript',
  'Nuxt',
  'Tailwindcss',
  'Drizzle ORM',
  'SQL',
  'SQLite3',
  'Cloudfare D1',
  'Cloudfare Pages',
  'Google APIs',
  'Google Console',
  'GitHub'
]

</script>

<style>
.tech-section {
  transition: all 300ms;
  transform-origin: center;
}
.tech-section:hover {
  transform: scale(1.02);
}
</style>