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
    <div class="m-4 grid grid-cols-2 xs:grid-rows-1">   
      <h1 class="m-2 xs:-m-3 p-2 xs:p-0 max-h-6 inline">
        About Guillermo Kababbe Development Services
      </h1>
      <div v-if="isAbove('md')" class="m-2 p-2 flex justify-center">
        <p>Some of my projects: </p>
        <SlideProjectList />
      </div>
    </div>
  </section>
</template>
