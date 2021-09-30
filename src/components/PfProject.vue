<template>
  <a
    class="card-project"
    rel="noopener noreferrer"
    target="_blank"
    :href="'https://github.com/jasba24/' + href"
  >
    <img :src="logo" alt="proyecto image" class="card-image" />
    <button>
      See project
    </button>
  </a>
</template>

<script setup>
defineProps(["logo", "href"])
</script>

<style src="../assets/css/project.css"></style>
