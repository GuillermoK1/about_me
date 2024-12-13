<script setup lang="ts">
const links = [{
  label: 'Check my github repositories.',
  icon: 'i-heroicons-folder-20-solid',
  badge: 'GuillermoK1',
  to: 'https://github.com/GuillermoK1'
}, {
  label: 'No license for this site.',
  icon: 'i-heroicons-document-solid',
  badge: 'Made with heart',
}, {
  label: 'Contact',
  icon: 'i-heroicons-document-solid',
  badge: 'guillermojkr@gmail.com'
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
