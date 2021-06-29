<template>
  <section class="skills">
    <h1>Skills</h1>
    <ul class="skills-list">
      <li v-for="(s, i) in skills" :key="i">
        <img :src="s.icon" :alt="s.name" :title="s.name" />
      </li>
    </ul>
  </section>
</template>

<script>
import bulma from "@/assets/icon/bulma.png";
import css from "@/assets/icon/css.svg";
import GitYGitHub from "@/assets/icon/GitYGitHub.jpg";
import vue from "@/assets/icon/vue.svg";
import react from "@/assets/icon/react.svg";
import html from "@/assets/icon/html.svg";
import rest from "@/assets/icon/rest.png";
import stylus from "@/assets/icon/stylus.svg";
import tailwind from "@/assets/icon/tailwind.svg";
import js from "@/assets/icon/js.svg";

export default {
  name: "Skills",

  data() {
    return {
      skills: [
        {
          icon: html,
          name: "HTML"
        },
        {
          icon: css,
          name: "CSS"
        },
        {
          icon: stylus,
          name: "STYLUS"
        },
        {
          icon: tailwind,
          name: "TAILWIND"
        },
        {
          icon: bulma,
          name: "BULMA"
        },
        {
          icon: js,
          name: "JS"
        },
        {
          icon: vue,
          name: "VUE"
        },
        {
          icon: react,
          name: "REACT"
        },
        {
          icon: rest,
          name: "APIs REST"
        },
        {
          icon: GitYGitHub,
          name: "GIT Y GITHUB"
        }
      ]
    };
  }
};
</script>

<style scoped>
.skills {
  display: flex;
  text-align: center;
  flex-direction: column;
}
.skills h1 {
  margin-bottom: 20px;
}
.skills-list {
  display: grid;
  justify-content: center;
  align-items: center;
  grid-template-columns: repeat(5, 1fr);
  font-size: 2rem;
  margin-bottom: 20px;
  gap: 10px;
}
.skills-list li {
  list-style: none;
}
.skills-list img {
  width: 100px;
  height: 100px;
  border: none;
  cursor: pointer;
}
</style>