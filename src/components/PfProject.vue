<template>
  <section class="card-project">
    <img :src="logo" alt="imagen del proyecto" class="card-image" />
    <a target="_blank" :href="'https://github.com/jasba24/' + href">
      <button>
        See project
        <img :src="icon" class="button-icon" />
      </button>
    </a>
  </section>
</template>

<script>
export default {
  name: "Project",

  props: ["icon", "logo", "href"]
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
  box-shadow: 0px 6px 7px 2px gray;
}
img {
  width: 300px;
  height: 200px;
  margin-bottom: 10px;
  border: 0.1px solid gray;
}
.card-project a button {
  height: 50px;
  width: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--primary-color);
  font-weight: bold;
  font-size: 2.5rem;
}
.button-icon {
  width: 25px;
  height: 25px;
  margin-left: 10px;
}
</style>