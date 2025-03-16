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
  { id: 1, text: 'I love your products!', author: 'apricitestudios.com' },
  { id: 2, text: 'I love your products!', author: 'flashdata slu' },
  { id: 3, text: 'I love your products!', author: 'Lauri Saar' },
]
</script>