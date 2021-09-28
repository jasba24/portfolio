<template>
  <div class="home">
    <Hero></Hero>
    <Skills></Skills>
    <section class="projects">
      <h1>Projects</h1>
      <div class="projects-container">
        <Project
          v-for="(p, i) in projects"
          :logo="p.logo"
          :href="p.href"
        ></Project>
      </div>
    </section>
  </div>
</template>

<script setup>
import platziBadges from "@/assets/platzi-badges.png"
import exchange from "@/assets/exchange.png"
import platziMusic from "@/assets/platzi-music.png"
import Hero from "@/components/PfHero"
import Skills from "@/components/PfSkills"
import Project from "@/components/PfProject"
import { ref } from "vue"

const projects = ref([
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
])
</script>
