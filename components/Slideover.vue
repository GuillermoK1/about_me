<script setup lang="ts">
const isOpen = ref(false)
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
  <div>
    <UButton icon="i-heroicons-bars-3" color="gray" @click="isOpen = true" />

    <USlideover v-model="isOpen" :transition="false" class="w-52 " >
      <div class="p-4 max-w-52">
        <UButton
          color="gray"
          variant="ghost"
          size="sm"
          icon="i-heroicons-x-mark-20-solid"
          class="flex sm:hidden absolute end-5 top-5 z-10"
          square
          padded
          @click="isOpen = false"
        />

        <UVerticalNavigation :links="links" />
        <p class="p-2">Or choose a project...</p>
        <SelectMenu />
      </div>
    </USlideover>
  </div>
</template>

