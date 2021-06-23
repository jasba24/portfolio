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
          :icon="p.icon"
          :href="p.href"
        ></Project>
      </div>
    </section>
  </div>
</template>

<script>
import platziBadges from "@/assets/platzi-badges.png";
import exchange from "@/assets/exchange.png";
import platziMusic from "@/assets/platzi-music.png";
import icon from "@/assets/logo.png";
import Hero from "@/components/PfHero";
import Skills from "@/components/PfSkills";
import Project from "@/components/PfProject";

export default {
  name: "Home",
  components: { Hero, Skills, Project },

  data() {
    return {
      projects: [
        {
          logo: platziBadges,
          icon: icon,
          href: "Platzi-badges"
        },
        {
          logo: exchange,
          icon: icon,
          href: "Platzi-exchange"
        },
        {
          logo: platziMusic,
          icon: icon,
          href: "Platzi-badges"
        }
      ]
    };
  }
};
</script>
