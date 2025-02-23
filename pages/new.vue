<template>
  <div class="container mx-auto px-4 py-8">
    <h1 class="text-3xl font-bold text-center mb-8 dark:text-white">Web App Starter Template</h1>
    
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <!-- Feature Cards -->
      <div v-for="(feature, index) in features" :key="index" 
           class="p-6 rounded-lg border border-slate-200 dark:border-slate-700 hover:shadow-lg transition-shadow">
        <div class="flex items-center mb-4">
          <component :is="feature.icon" class="w-6 h-6 text-blue-500"/>
          <h3 class="ml-2 font-semibold dark:text-white">{{ feature.title }}</h3>
        </div>
        <p class="text-slate-600 dark:text-slate-300">{{ feature.description }}</p>
      </div>
    </div>

    <div class="mt-12 text-center">
      <h2 class="text-2xl font-semibold mb-3 dark:text-white">Ready to start your project?</h2>
      <p class="text-slate-600 dark:text-slate-300">Choose your preferred contact method below to get in touch</p>
    </div>
  </div>
</template>

<script setup lang="ts">

const features = [
  {
    title: 'Dark/Light Mode',
    description: 'Toggle between dark and light themes with a single click',
    icon: 'i-heroicons-moon'
  },
  {
    title: 'Google OAuth 2.0',
    description: 'Secure authentication with Google OAuth integration',
    icon: 'i-heroicons-lock-closed'
  },
  {
    title: 'Protected Routes',
    description: 'Restrict access to authenticated users only',
    icon: 'i-heroicons-shield-check'
  },
  {
    title: 'SEO Optimized',
    description: 'Built-in SEO best practices for better visibility',
    icon: 'i-heroicons-globe-alt'
  },
  {
    title: 'Responsive Design',
    description: 'Fully responsive layout that works on all devices',
    icon: 'i-heroicons-device-phone-mobile'
  },
  {
    title: 'Cloud Hosted',
    description: 'Ready for deployment to your preferred cloud platform',
    icon: 'i-heroicons-cloud'
  },
  {
    title: 'Modern UI Components',
    description: 'Beautiful, ready-to-use UI components',
    icon: 'i-heroicons-circle-stack'
  },
  {
    title: 'Customizable Style',
    description: 'Easy to customize design system with Tailwind CSS',
    icon: 'i-heroicons-paint-brush'
  },
  {
    title: 'Lightweight',
    description: 'Optimized for performance and fast loading times',
    icon: 'i-heroicons-arrow-path'
  }
]
</script>