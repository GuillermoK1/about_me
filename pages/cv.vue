<script setup lang="ts">
const selected = ref(false)
</script>

<template>
    <div class="flex m-1">
        <UToggle
        v-model="selected"
        onIcon="i-heroicons-language"
        offIcon="i-heroicons-language"
        color="sky"
        class="mr-2"
        />
        <p v-if="selected" ><strong>Español</strong> / English</p>
        <p v-else><strong>English</strong> / Español</p>
    </div>
    <div v-if="selected">
        <iframe src="/assets/CVs/CV ATS_es.pdf" width="100%" class="h-[50vh] rounded-lg"></iframe>
    </div>
    <div v-else>
        <iframe src="/assets/CVs/CV ATS_en.pdf" width="100%" class="h-[50vh] rounded-lg"></iframe>
    </div>
</template>