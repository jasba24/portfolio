<template>
  <div class="home">
    <Hero></Hero>
    <Skills></Skills>
    <h1>Projects</h1>
    <section class="projects">
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
import logo from "@/assets/logo.png";
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
          logo: logo,
          icon: icon,
          href: "Platzi-badges"
        },
        {
          logo: logo,
          icon: icon,
          href: "Platzi-rooms"
        },
        {
          logo: logo,
          icon: icon,
          href: "Platzi-badges"
        }
      ]
    };
  }
};
</script>

