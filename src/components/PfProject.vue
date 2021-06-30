<template>
  <a
    class="card-project"
    target="_blank"
    :href="'https://github.com/jasba24/' + href"
  >
    <img :src="logo" alt="imagen del proyecto" class="card-image" />
    <button>
      See project
    </button>
  </a>
</template>

<script>
export default {
  name: "Project",

  props: ["logo", "href"]
};
</script>

<style>
.card-project {
  width: 350px;
  height: 300px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10px;
  box-shadow: 0px 6px 7px 2px var(--primary-color);
}
img {
  width: 300px;
  height: 200px;
  margin-bottom: 10px;
  border: 0.1px solid gray;
}
.card-project button {
  height: 50px;
  width: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  color: white;
  font-weight: bold;
  font-size: 2.5rem;
  background-color: var(--primary-color);
}
</style>