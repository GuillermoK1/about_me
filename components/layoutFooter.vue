<script setup lang="ts">
const links = [{
  label: 'My github repositories.',
  icon: 'i-heroicons-folder-20-solid',
  to: 'https://github.com/GuillermoK1'
},
{
  label: 'info@gkdevservices.com',
  icon: 'i-heroicons-envelope-solid',
},
{
  label: 'LinkedIn profile',
  icon: 'i-heroicons-linkedin-solid',
  to: 'https://www.linkedin.com/in/gkdevservices/'
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
