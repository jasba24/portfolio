<template>
  <footer
    class="footer"
    :class="{ bottom: addStyle ? true : false }"
    id="footer"
  >
    <h1 class="footer-title">Contact me</h1>
    <h1 class="footer-title">
      Made with <img :src="logo" alt="vue.js icon" />
    </h1>
    <div class="links-container">
      <a
        class="footer-link"
        rel="noopener noreferrer"
        target="_blank"
        v-for="(l, i) in links"
        :key="i"
        :href="l.href"
      >
        {{ l.name }}
      </a>
    </div>
  </footer>
</template>

<script setup>
import logo from "@/assets/logo.png"
import { ref, computed } from "vue"
import { useRoute } from "vue-router"

const route = useRoute()

const links = ref([
  {
    name: "LinkedIn",
    href: "https://linkedin.com/in/jasba24",
  },
  {
    name: "Twitter",
    href: "https://twitter.com/jasba24",
  },
  {
    name: "GitHub",
    href: "https://github.com/jasba24",
  },
])

const addStyle = computed(() => {
  if (route.name === "About" || route.name === "Blog") {
    return true
  } else {
    return false
  }
})
</script>

<style scoped src="../assets/css/footer.css"></style>
