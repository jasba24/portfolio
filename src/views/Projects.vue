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
import diabloe3 from "@/assets/diabloe3.png";
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
          href: "Platzi-badges"
        },
        {
          logo: diabloe3,
          icon: icon,
          href: "Platzi-badges"
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

<style scoped>
.projects {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.projects h1 {
  margin: 20px 0;
}
.projects-container {
  display: grid;
  width: 800px;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}
</style>