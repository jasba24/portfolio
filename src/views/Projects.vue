<template>
  <div class="projects">
    <h1>Projects</h1>
    <div class="projects-container">
      <Project
        v-for="(p, i) in projects"
        :logo="p.logo"
        :href="p.href"
      ></Project>
    </div>
  </div>
</template>

<script setup>
import platziBadges from "@/assets/platzi-badges.png"
import exchange from "@/assets/exchange.png"
import platziMusic from "@/assets/platzi-music.png"
import diablo3 from "@/assets/diablo3.png"
import spa from "@/assets/spa.png"
import hackaton from "@/assets/hackaton.png"
import Project from "@/components/PfProject"
import { ref } from "vue"

const projects = ref([
  {
    logo: spa,
    href: "SPA-JS",
  },
  {
    logo: diablo3,
    href: "diabloe3-vue",
  },
  {
    logo: platziBadges,
    href: "Platzi-bagdes",
  },
  {
    logo: exchange,
    href: "Platzi-exchange-vue",
  },
  {
    logo: platziMusic,
    href: "Platzi-music-vue",
  },
  {
    logo: hackaton,
    href: "hackatonProject",
  },
])
</script>
