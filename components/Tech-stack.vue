<template>
  <div class="p-6 bg-gray-50 dark:bg-gray-800 rounded-lg shadow-lg">
    <div class="grid grid-cols-3 gap-8">
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

      <!-- DevOps Cycle -->
      <div class="tech-section">
        <h3 class="text-xl font-bold mb-4 text-blue-600 dark:text-blue-400">
          DevOps Cycle
        </h3>
        <div class="flex flex-wrap gap-4 items-center justify-center">
          <div v-for="(step, index) in devOpsCycle" :key="step" 
            class="flex items-center">
            <span class="px-4 py-2 bg-blue-100 dark:bg-blue-900 rounded-lg text-blue-700 dark:text-blue-300">
              {{ step }}
            </span>
            <svg v-if="index < devOpsCycle.length - 1" class="h-4 w-4 mx-2 text-blue-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </div>
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
  'Google C. P.'
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

const devOpsCycle = [
  'Code',
  'Build',
  'Test',
  'Deploy',
  'Monitor',
  'Scale',
  'Repeat'
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