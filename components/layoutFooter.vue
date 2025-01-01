<script setup lang="ts">
const links = [{
  label: 'Check my github repositories.',
  icon: 'i-heroicons-folder-20-solid',
  to: 'https://github.com/GuillermoK1'
}, {
  label: 'MIT License',
  icon: 'i-heroicons-document-solid',
}, {
  label: 'Contact',
  icon: 'i-heroicons-envelope-solid',
}]
</script>

<template>
  <section>
    <UVerticalNavigation
    :links="links"
    class="w-4/5"
    :ui="{
      label: 'text-gray-900 dark:text-white'
    }"
  >
  </UVerticalNavigation>
  </section>
</template>
