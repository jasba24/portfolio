<template>
  <Header :links="headerLinks"></Header>
  <router-view></router-view>
  <Footer></Footer>
</template>

<script>
import Header from "@/components/PfHeader"
import Footer from "@/components/ PfFooter"

export default {
  name: "App",
  components: { Header, Footer },
  data() {
    return {
      headerLinks: [
        {
          name: "About",
          href: "/about",
        },
        {
          name: "Blog",
          href: "/blog",
        },
        {
          name: "Projects",
          href: "/projects",
        },
      ],
    }
  },
}
</script>

<style>
:root {
  --primary-color: #00b7c2;
  --box-color: #00b7c2;
  --bg-color: #1b262c;
  --button-color: #00b7c2;
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

body {
  background: var(--bg-color);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: var(--primary-color);
}
.projects {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.projects h1 {
  margin: 20px 0;
}
.projects-container {
  display: grid;
  margin: 0 auto;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}
.footer.bottom {
  position: absolute;
  bottom: 0;
  width: 100%;
  margin: 0;
}
</style>
