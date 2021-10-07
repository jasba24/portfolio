<template>
  <section class="skills">
    <h1>Skills</h1>
    <ul class="skills-list">
      <li v-for="(s, i) in skills" :key="i" class="skills-item-container">
        <span class="skills-img-title" :ref="s.name">{{ s.name }}</span>
        <img
          @mouseover="showImgTitle(s.name)"
          @mouseleave="showImgTitle(s.name)"
          :src="s.icon"
          :alt="s.name.toLowerCase() + ' icon'"
        />
      </li>
    </ul>
  </section>
</template>

<script>
import bulma from "@/assets/icon/bulma.png"
import css from "@/assets/icon/css.png"
import GitYGitHub from "@/assets/icon/GitYGitHub.png"
import vue from "@/assets/icon/vue.png"
import react from "@/assets/icon/react.png"
import html from "@/assets/icon/html.png"
import nodejs from '@/assets/icon/nodejs.png'
import stylus from "@/assets/icon/stylus.png"
import tailwind from "@/assets/icon/tailwind.png"
import js from "@/assets/icon/js.png"

export default {
  name: "Skills",

  data() {
    return {
      skills: [
        {
          icon: html,
          name: "HTML",
        },
        {
          icon: css,
          name: "CSS",
        },
        {
          icon: stylus,
          name: "STYLUS",
        },
        {
          icon: tailwind,
          name: "TAILWIND",
        },
        {
          icon: bulma,
          name: "BULMA",
        },
        {
          icon: js,
          name: "JS",
        },
        {
          icon: vue,
          name: "VUE",
        },
        {
          icon: react,
          name: "REACT",
        },
        {
          icon: nodejs,
          name: "NODEJS",
        },
        {
          icon: GitYGitHub,
          name: "GIT Y GITHUB",
        },
      ],
    }
  },

  methods: {
    showImgTitle(item) {
      this.$refs[item].classList.toggle("show-title")
      if (item === "GIT Y GITHUB") {
        this.$refs[item].innerHTML = `GIT Y <br /> GITHUB`
      }
    },
  },
}
</script>

<style scoped src="../assets/css/skills.css"></style>
