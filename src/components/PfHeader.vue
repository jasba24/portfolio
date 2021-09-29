<template>
  <header class="header">
    <router-link to="/" class="header-title">Johan Buitrago</router-link>
    <div>
      <router-link
        v-for="(l, i) in links"
        :key="i"
        class="header-link"
        :to="l.href"
      >
        {{ l.name }}
      </router-link>
      <router-link class="header-link" to="#footer" hash="#footer">
        Contact
      </router-link>
    </div>
  </header>
</template>

<script setup>
defineProps(["links"])
</script>

<style scoped src="../assets/css/header.css"></style>
