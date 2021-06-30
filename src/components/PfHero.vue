<template>
  <section class="hero">
    <h1>I'm a frontend developer</h1>
    <p>Excited to meet new projects where I can develop me and learn more</p>
  </section>
</template>

<script>
export default {
	name: "Hero"
};
</script>

<style>
.hero {
  height: calc(100vh - 70px);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-align: center;
  background: radial-gradient(
      50% 50% at 50% 50%,
      rgba(26, 21, 21, 0) 0%,
      rgba(1, 1, 1, 0.16) 100%
    ),
    #ffffff;
}
.hero h1 {
  margin-bottom: 20px;
	font-size: 6rem;
}
.hero p {
  font-size: 3rem;
}
</style>