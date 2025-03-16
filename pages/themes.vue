<script setup lang="ts">
import { useColor } from '../composables/useColors'

const { primaryColor, secondaryColor, setPrimaryColor, setSecondaryColor } = useColor()

const handlePrimaryChange = (e: Event) => {
  const target = e.target as HTMLInputElement
  setPrimaryColor(target.value)
}

const handleSecondaryChange = (e: Event) => {
  const target = e.target as HTMLInputElement
  setSecondaryColor(target.value)
}
</script>

<template>
    <h2 class="m-4 p-2">
        Themes is my open source project powered by Nuxt3 and TailwindCSS.<br>
        The main goal of this project is to provide a simple and easy way to create a new theme for your website or page,
        the proyect is currently in expansion, offering a variety of ways to customize your theme.
    </h2>
    <!-- Color Selectors -->
    <section class="flex ml-4 w-fit rounded-lg shadow-lg bg-gray-200 dark:bg-gray-800">
        <div class="m-4 p-2 flex flex-col gap-4">
            <div class="flex items-center gap-4">
                <label>Primary Color:</label>
                <input 
                    type="color" 
                    :value="primaryColor"
                    @change="handlePrimaryChange"
                    class="w-24 h-12 rounded-md cursor-pointer border-2"
                />
            </div>
            <div class="flex items-center gap-4">
                <label>Secondary Color:</label>
                <input 
                    type="color" 
                    :value="secondaryColor"
                    @change="handleSecondaryChange"
                    class="w-24 h-12 rounded-md cursor-pointer border-2"
                />
            </div>
        </div>
        
        <!-- Demo Card -->
        <div class="m-4 p-2">
            <div class="max-w-sm rounded-lg shadow-lg p-6" :style="{ backgroundColor: primaryColor }">
                <h3 class="text-xl font-bold mb-2" :style="{ color: secondaryColor }">Demo Card</h3>
                <p class="text-base" :style="{ color: secondaryColor }">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                </p>
            </div>
        </div>
    </section>
    <u><a class="font-serif m-4 p-2 text-xl text-sky-900 dark:text-sky-400" href="https://themeselector.pages.dev">Playground</a></u>
    <div class="m-2 p-2 gap-8 grid grid-cols-2 justify-around">
        <img class="w-full max-w-96 aspect-square" src='../public/assets/themes/dark-orange.png' />
        <img class="w-full max-w-96 aspect-square" src='../public/assets/themes/light-indigo.png' />
    </div>
</template>