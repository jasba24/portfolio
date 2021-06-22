<template>
  <Header></Header>
  <router-view></router-view>
</template>

<script>
import Header from "@/components/PfHeader";

export default {
  name: "App",
  components: { Header }
};
</script>

<style>
:root {
  --primary-color: #2c3e50;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
}

h1 {
  font-size: 3.2rem;
}

a {
  color: inherit;
  text-decoration: none;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: var(--primary-color);
}
</style>
