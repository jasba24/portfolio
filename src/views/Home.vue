<template>
  <div class="home">
    <Hero></Hero>
    <Skills></Skills>
  </div>
</template>

<script>
import Hero from "@/components/PfHero";
import Skills from '@/components/PfSkills'

export default {
  name: "Home",
  components: { Hero, Skills }
};
</script>
