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
    <section class="flex flex-col md:flex-row ml-4 w-[95%] md:w-fit rounded-lg shadow-lg bg-gray-200 dark:bg-gray-800 overflow-x-hidden">
        <div class="m-4 p-6 flex flex-col gap-4 bg-gradient-to-b from-sky-400 via-indigo-500 to-orange-500 dark:from-sky-800 dark:via-indigo-800 dark:to-orange-800 rounded-lg shadow-lg max-w-sm w-auto">

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
        
        <!-- Demo card -->
        <div class="m-4 w-auto">
            <div class="max-w-sm rounded-lg shadow-lg p-6" :style="{ backgroundColor: primaryColor }">
                <h3 class="text-xl font-bold mb-2" :style="{ color: secondaryColor }">Demo Card</h3>
                <p class="text-base" :style="{ color: secondaryColor }">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                </p>
            </div>
        </div>
        <!-- Playground card -->
        <div class="m-4 w-auto">
            <div class="max-w-sm rounded-lg shadow-lg p-6 bg-lime-800">
                <a class="font-serif m-4 p-2 text-xl text-sky-400" href="https://themeselector.pages.dev">Playground</a>
                <div class="m-2 p-2">
                    <img class="w-full rounded-lg" src='../public/assets/themes/capture.png' alt="screenshot" />
                </div>
            </div>
        </div>
    </section>
</template>