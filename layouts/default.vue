<script setup lang="ts">
import LayoutHeader from '~/components/layoutHeader.vue';
import LayoutPages from '~/components/layoutPages.vue';
</script>

<template>
    <section class="w-full h-[90vh] p-2 grid grid-templates-rows-6 space-y-2">
        <LayoutHeader class="row-span-1 ring-2 ring-black dark:ring-white"/>
        <LayoutPages class="row-span-5 ring-2 ring-black dark:ring-white"/>
        <LayoutFooter class="row-span-1 ring-2 ring-black dark:ring-white"/>
    </section>
</template>