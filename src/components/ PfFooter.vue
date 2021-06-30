<template>
  <footer
    class="footer"
    :class="{ bottom: addStyle ? true : false }"
    id="footer"
  >
    <h1 class="footer-title">Contact me</h1>
    <h1 class="footer-title">Made with <img :src="logo" alt="vue.js icon" /></h1>
    <div>
      <a
        class="footer-link"
        target="_blank"
        v-for="(l, i) in links"
        :key="i"
        :href="l.href"
      >
        {{ l.name }}
      </a>
    </div>
  </footer>
</template>

<script>
import logo from "@/assets/logo.png";

export default {
  name: "footer",
  data() {
    return {
      logo,
      links: [
        {
          name: "LinkedIn",
          href: "https://linkedin.com/in/jasba24"
        },
        {
          name: "Twitter",
          href: "https://twitter.com/jasba24"
        },
        {
          name: "GitHub",
          href: "https://github.com/jasba24"
        }
      ]
    };
  },

  computed: {
    addStyle() {
      if (this.$route.name === "About" || this.$route.name === "Blog") {
        return true;
      } else {
        return false;
      }
    }
  }
};
</script>

<style scoped>
.footer {
  height: 70px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 50px;
  box-shadow: -2px -6px 7px 0 var(--box-color);
  margin-top: 40px;
}
.footer-title {
  font-size: 3.2rem;
  font-weight: bold;
}
.footer-title img {
  width: 40px;
  height: 40px;
  border: none;
  margin-bottom: 0;
}
.footer-link {
  font-size: 1.6rem;
  margin-left: 10px;
  font-weight: bold;
  cursor: pointer;
}
</style>

