<template>
  <footer class="footer">
    <h1 class="footer-title">Contact me</h1>
    <div>
      <a
        target="_blank"
        v-for="(l, i) in links"
        :key="i"
        class="footer-link"
        :href="l.href"
      >
        {{ l.name }}
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  name: "footer",
  props: ["links"]
};
</script>

<style scoped>
.footer {
  height: 70px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 50px;
  box-shadow: -2px -6px 7px 0 grey;
  margin-top: 40px;
}
.footer-title {
  font-size: 3.2rem;
  font-weight: bold;
}
.footer-link {
  font-size: 1.6rem;
  margin-left: 10px;
  font-weight: bold;
  cursor: pointer;
}
</style>

