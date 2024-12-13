<template>
    <section class="topography p-4 grid grid-templates-rows-6 space-y-2 w-dvw">
        <LayoutHeader class="backdrop-opacity-10 bg-slate-400/90 dark:bg-slate-600/90 row-span-1 ring-2 ring-black dark:ring-white h-fit w-full"/>
        <LayoutPages class="backdrop-opacity-10 bg-slate-400/90 dark:bg-slate-600/90 row-span-5 ring-2 ring-black dark:ring-white rounded-lg h-fit w-full"/>
        <LayoutFooter class="backdrop-opacity-10 bg-slate-400/90 dark:bg-slate-600/90 row-span-1 ring-2 ring-black dark:ring-white h-fit w-full"/>
    </section>
</template>
<style lang="css" scoped>
.topography {
  background-image: url('../public/assets/topography.svg');
}
</style>