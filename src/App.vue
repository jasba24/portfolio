<template>
  <Header :links="links"></Header>
  <router-view></router-view>
</template>

<script>
import Header from "@/components/PfHeader";

export default {
  name: "App",
  components: { Header },
  data() {
    return {
      links: [
        {
          name: "About",
          href: "/about"
        },
        {
          name: "Blog",
          href: "/blog"
        },
        {
          name: "Projects",
          href: "/projects"
        },
        {
          name: "Contact",
          href: "/contact"
        }
      ]
    };
  }
};
</script>

<style>
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
  color: #2c3e50;
}
</style>
