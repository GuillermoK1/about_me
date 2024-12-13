<script setup lang="ts">
const links = [
  {
    label: 'PLASMA',
    to: '/plasma'
  },
  {
    label: 'Python',
    to: '/python'
  },
  {
    label: 'Themes',
    to: '/themes'
  },
  {
    label: 'New',
    to: '/new'
  }]
</script>

<template>
    <UVerticalNavigation :links="links" />
</template>