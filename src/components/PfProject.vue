<template>
  <section class="card-project">
    <img :src="logo" alt="imagen del proyecto" class="card-image" />
  </section>
</template>

<script>
import logo from "@/assets/logo.png";
export default {
  name: "Project",

  data() {
    return {
      logo: logo
    };
  }
};
</script>

<style>
</style>