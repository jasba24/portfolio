<template>
  <div class="projects">
    <h1>Projects</h1>
    <div class="projects-container">
      <Project
        v-for="(p, i) in projects"
        :logo="p.logo"
        :icon="p.icon"
        :href="p.href"
      ></Project>
    </div>
  </div>
</template>

<script>
import platziBadges from "@/assets/platzi-badges.png";
import exchange from "@/assets/exchange.png";
import platziMusic from "@/assets/platzi-music.png";
import diablo3 from "@/assets/diablo3.png";
import spa from "@/assets/spa.png";
import icon from "@/assets/logo.png";
import Project from "@/components/PfProject";

export default {
  name: "Projects",
  components: { Project },

  data() {
    return {
      projects: [
        {
          logo: spa,
          icon: icon,
          href: "SPA-JS"
        },
        {
          logo: diablo3,
          icon: icon,
          href: "diabloe3-vue"
        },
        {
          logo: platziBadges,
          icon: icon,
          href: "Platzi-badges"
        },
        {
          logo: exchange,
          icon: icon,
          href: "Platzi-exchange-vue"
        },
        {
          logo: platziMusic,
          icon: icon,
          href: "Platzi-music-vue"
        },
        {
          logo: icon,
          icon: icon,
          href: "Platzi-badges"
        }
      ]
    };
  }
};
</script>