<script setup lang="ts">
import { useBreakpoint } from '~/composables/useBreakpoint';

const { currentBreakpoint, isAbove } = useBreakpoint();
</script>

<template>
  <section class="mt-4 h-fit grid grid-template-rows-2 bg-sky-300 dark:bg-sky-900">
    <h1 class="place-self-center">
        About Guillermo Kabbabe
    </h1>
    <div class="flex place-content-start">
      <UBadge
        icon="i-heroicons-window"
        size="sm"
        color="gray"
        label="Current breakpoint: "
      />
      {{ currentBreakpoint }}
    </div>
    <HorizontalNavigation v-if="isAbove('md')" />
    <Slideover v-else />
  </section>
</template>
