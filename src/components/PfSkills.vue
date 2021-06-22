<template>
  <section class="skills">
    <h1>Skills</h1>
    <ul class="skills-list">
      <li v-for="(s, i) in skills" :key="i">{{ s }}</li>
    </ul>
  </section>
</template>

<script>
export default {
  name: "Skills",

  data() {
    return {
      skills: [
        "HTML",
        "CSS",
        "Stylus",
        "Tailwind",
        "Bulma",
        "JavaScript",
        "Vue",
        "React",
        "APIs REST",
        "Git y GitHub"
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
</style>