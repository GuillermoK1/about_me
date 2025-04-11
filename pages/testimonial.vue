<template>
  <section>
    <h1>Testimonials</h1>
    <p>Here are some testimonials from our customers:</p>
    <ul>
      <li v-for="testimonial in testimonials" :key="testimonial.id">
        <blockquote>{{ testimonial.text }}</blockquote>
        <cite>{{ testimonial.author }}</cite>
      </li>
    </ul>
  </section>
</template>

<script setup lang="ts">
const testimonials = [
  { id: 1, text: 'Coming soon...', author: 'apricitestudios.com' },
  { id: 2, text: 'Coming soon...', author: 'flashdata slu' },
  { id: 3, text: 'Coming soon...', author: 'Lauri Saar' },
]
</script>