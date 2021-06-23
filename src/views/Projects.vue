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
import logo from "@/assets/logo.png";
import icon from "@/assets/logo.png";
import Project from "@/components/PfProject";

export default {
  name: "Projects",
  components: { Project },

  data() {
    return {
      projects: [
        {
          logo: logo,
          icon: icon,
          href: "Platzi-badges",
        },
        {
          logo: logo,
          icon: icon,
          href: "Platzi-rooms",
        },
        {
          logo: logo,
          icon: icon,
          href: "Platzi-badges",
        },
        {
          logo: logo,
          icon: icon,
          href: "Platzi-badges",
        },
        {
          logo: logo,
          icon: icon,
          href: "Platzi-badges",
        },
        {
          logo: logo,
          icon: icon,
          href: "Platzi-badges",
        }
      ]
    };
  }
};
</script>

<style>
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
  margin: 0 auto;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}
</style>