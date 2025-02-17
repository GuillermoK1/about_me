<script setup lang="ts">
const isOpen = ref(false)
</script>

<template>
  <div>
    <UButton icon="i-heroicons-book-open" color="gray" @click="isOpen = true" />
    <USlideover v-model="isOpen" side="right" class="w-auto" >
      <div class="p-4 w-auto">
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
        <Tech-stack/>
      </div>
    </USlideover>
  </div>
</template>
