<template>
  <section class="profile">
    <h1 class="profile-title">I am Johan Buitrago</h1>
    <p>
      I'm looking to collaborate in a company where I can develop Web
      applications
    </p>
    <p>
      using my Skills as a Frontend Developer in the company of a great team.
    </p>
    <p>
      Actually I work with Vue.js, React.js and Nuxt.
    </p>
  </section>
</template>

<script>
export default {
  name: "Profile"
};
</script>

<style>
.profile {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
h1 {
  margin: 20px 0;
}
p {
  font-size: 2rem;
  margin-bottom: 10px;
}
</style>