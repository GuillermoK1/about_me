<script setup lang="ts">
import { useBreakpoint } from '~/composables/useBreakpoint';

const { currentBreakpoint, isAbove } = useBreakpoint();
</script>

<template>
  <section class="mt-4 h-fit flex place-content-between bg-sky-300 dark:bg-sky-900">
    <h1 class="p-4">
        About Guillermo Kababbe Development Services
    </h1>
    <HorizontalNavigation v-if="isAbove('md')" class="p-4" />
    <div v-else class="p-4">
      <Slideover class="flex justify-end"/>
      <div>
      <p class="p-2">Or choose a project...</p>
      <SelectMenu />
      </div>
    </div>
    
  </section>
</template>
