<script setup lang="ts">
const links = [{
  label: 'github',
  icon: 'i-heroicons-folder-20-solid',
  badge: 'GuillermoK1',
}, {
  label: 'license',
  icon: 'i-heroicons-document-solid',
  badge: 'License',
}, {
  label: 'contact',
  icon: 'i-heroicons-document-solid',
  badge: 'Contact',
}]
</script>

<template>
  <UVerticalNavigation
    :links="links"
    class="w-full"
    :ui="{
      label: 'text-gray-900 dark:text-white'
    }"
  >
  </UVerticalNavigation>
</template>

