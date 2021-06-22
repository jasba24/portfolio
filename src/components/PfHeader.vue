<template>
  <header class="header">
    <h1>Johan Buitrago</h1>
    <div>
      <a v-for="(l, i) in links" :key="i" class="header-link" :href="l.href">{{
        l.name
      }}</a>
    </div>
  </header>
</template>

<script>
export default {
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
          href: "#about"
        }
      ]
    };
  }
};
</script>

<style scoped>
.header {
  height: 70px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 50px;
  box-shadow: 2px 6px 7px 0 grey;
}

.header-link {
  color: inherit;
  text-decoration: none;
  font-size: 1.6rem;
  margin-left: 10px;
  font-weight: bold;
}
</style>