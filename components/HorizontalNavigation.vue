<script setup lang="ts">
const links = [{
  avatar: {
    src: '',
    alt: 'GK',
    size: 'md'
  }
}, {
  label: 'Home',
  icon: 'i-heroicons-home',
  to: '/',
  labelClass: 'text-sky-950 dark:text-sky-200',
  iconClass: 'text-sky-950 dark:text-sky-200' 
}, {
  label: 'All projects',
  icon: 'i-heroicons-inbox-stack',
  to: '/projects',
  labelClass: 'text-sky-950 dark:text-sky-200',
  iconClass: 'text-sky-950 dark:text-sky-200' 
}, {
  label: 'Themes',
  icon: 'i-heroicons-paint-brush',
  to: '/themes',
  labelClass: 'text-sky-950 dark:text-sky-200',
  iconClass: 'text-sky-950 dark:text-sky-200' 
}]
</script>

<template>
  <UHorizontalNavigation :links="links" class="border-b border-gray-200 dark:border-gray-800"
  />
  <div class="p-2">
  <p class="p-2">Or choose a project...</p>
  <SelectMenu />
  </div>
</template>