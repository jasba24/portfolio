<template>
  <main class="post">
    <a
      class="post__link"
      rel="noopener noreferrer"
      :href="link"
      target="_blank"
    >
      <h1 class="post__title">{{ title }}</h1>
      <p class="post__time">{{ time }}</p>
      <p class="post__description">{{ description }}</p>
    </a>
  </main>
</template>

<script setup>
defineProps(["title", "description", "link", "time"])
</script>
