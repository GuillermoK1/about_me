<script setup lang="ts">
const links = [{
  avatar: {
    src: 'assets/profile_picture.jpg',
    alt: 'GK',
    size: 'xl'
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
    <UVerticalNavigation :links="links" />
</template>