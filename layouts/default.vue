<template>
    <section class="min-h-dvh w-full topography p-4 grid grid-rows-[auto_1fr_auto] gap-12">
        <LayoutHeader class="backdrop-blur-sm bg-slate-400/90 dark:bg-slate-600/90 ring-2 ring-black dark:ring-white h-fit w-full"/>
        <LayoutPages class="backdrop-blur-sm bg-slate-400/90 dark:bg-slate-600/90 ring-2 ring-black dark:ring-white rounded-lg min-h-72 w-full"/>
        <LayoutFooter class="backdrop-blur-sm bg-slate-400/90 dark:bg-slate-600/90 ring-2 ring-black dark:ring-white h-fit w-full"/>
    </section>
</template>

<style scoped>
.topography {
    background-image: url('/assets/topography.svg');
}
</style>