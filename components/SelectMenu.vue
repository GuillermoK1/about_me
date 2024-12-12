<template>
  <div class="flex">
    <UIcon name="i-heroicons-magnifying-glass" class="m-2 w-5 h-5"></UIcon>    
    <USelectMenu
        searchable
        searchable-placeholder="Search for a project"
        class="w-48"
        placeholder="Select a project"
        :options="['PLASMA', 'Python', 'Project 3', 'Project 4']"
        model-value="PLASMA"
      />
  </div>
</template>