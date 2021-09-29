<template>
  <main class="post">
    <h1 class="post__title">{{ title }}</h1>
    <p class="post__description">{{ description }}</p>
    <a
      class="post__link"
      rel="noopener noreferrer"
      :href="link"
      target="_blank"
    >
      <button>
        See Post
      </button>
    </a>
  </main>
</template>

<script setup>
defineProps(["title", "description", "link"])
</script>

<style src="../assets/css/post.css"></style>
