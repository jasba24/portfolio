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
        // {
        //   name: "About",
        //   href: "/about",
        // },
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

<style src="./index.css"></style>
