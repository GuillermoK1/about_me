<script setup lang="ts">
import { useBreakpoint } from '~/composables/useBreakpoint';

const { is } = useBreakpoint();
</script>

<template>
  <section class="p-4 flex justify-between w-fit" >
    <div v-if="is('xs')">
      <UAvatar
      src="assets/profile_picture.jpg"
      alt="profile picture"
      size="xl"
      />
      <Slideover/>
    </div>
    <VerticalNavigation v-else />
    <div class="m-4 grid grid-rows-2">   
      <h1 class="m-2 p-2 max-h-3 inline">
        About Guillermo Kababbe Development Services
      </h1>
      <div class="m-2 p-2 flex justify-center">
        <p>My proyects list</p>
        <SelectMenu />
      </div>
    </div>
  </section>
</template>
