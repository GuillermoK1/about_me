<script setup lang="ts">
import { useBreakpoint } from '~/composables/useBreakpoint';

const { is, isAbove } = useBreakpoint();
</script>

<template>
  <section class="p-4 flex justify-between w-fit" >
    <div v-if="is('2xs')">
      <UAvatar
      src="/assets/profile_picture.jpg"
      alt="profile picture"
      size="xl"
      />
      <Slideover/>
    </div>
    <VerticalNavigation v-else />
    <div class="m-4 grid grid-cols-1 md:grid-rows-2">   
      <h1 class="min-w-30 inline m-2 p-2 xl:text-2xl sm:text-md xs:text-xs font-bold bg-gradient-to-r from-blue-600 to-teal-600 bg-clip-text text-transparent hover:from-teal-600 hover:to-purple-600 transition-all duration-300">
        Guillermo Kabbabe Development Services
      </h1>
      <div v-if="isAbove('md')" class="m-2 p-2 gap-2 flex justify-center">
        <p>Technologies: </p>
        <SlideProjectList />
      </div>
    </div>
  </section>
</template>
