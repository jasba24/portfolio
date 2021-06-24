<template>
  <header class="header">
    <router-link to="/" class="header-title">Johan Buitrago</router-link>
    <div>
      <router-link
        v-for="(l, i) in links"
        :key="i"
        class="header-link"
        :to="l.href"
      >
        {{ l.name }}
      </router-link>
      <router-link class="header-link" to="#footer" hash="#footer">
        Contact
      </router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["links"]
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
.header-title {
  font-size: 3.2rem;
  font-weight: bold;
}
.header-link {
  font-size: 1.6rem;
  margin-left: 10px;
  font-weight: bold;
}
</style>

