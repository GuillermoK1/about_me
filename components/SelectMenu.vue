<template>
    <USelectMenu
        searchable
        searchable-placeholder="Search for a project"
        class="w-48"
        placeholder="Select a project"
        :options="['PLASMA', 'Project 1', 'Project 2', 'Project 3', 'Project 4', 'Project 5']"
        model-value="PLASMA"
      />
</template>