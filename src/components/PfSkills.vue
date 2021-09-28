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
import css from "@/assets/icon/css.svg"
import GitYGitHub from "@/assets/icon/GitYGitHub.png"
import vue from "@/assets/icon/vue.svg"
import react from "@/assets/icon/react.svg"
import html from "@/assets/icon/html.svg"
import rest from "@/assets/icon/rest.png"
import stylus from "@/assets/icon/stylus.svg"
import tailwind from "@/assets/icon/tailwind.svg"
import js from "@/assets/icon/js.svg"

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
          icon: rest,
          name: "APIs REST",
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
      if (item === "APIs REST") {
        this.$refs[item].innerHTML = `APIs <br /> REST`
      } else if (item === "GIT Y GITHUB") {
        this.$refs[item].innerHTML = `GIT Y <br /> GITHUB`
      }
    },
  },
}
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
  margin: 0 10px 20px;
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
.skills-item-container {
  position: relative;
}
.skills-img-title {
  position: absolute;
  color: white;
  background-color: black;
  border: 1px white solid;
  border-radius: 4px;
  padding: 2px;
  right: 0px;
  font-size: 15px;
  bottom: 50%;
  display: none;
}
.show-title {
  display: block;
}
</style>
