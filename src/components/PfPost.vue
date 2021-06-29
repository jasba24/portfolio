<template>
  <main class="post">
    <h1 class="post__title">{{ title }}</h1>
    <p class="post__description">{{ description }}</p>
    <a class="post__link" :href="link" target="_blank">
      <button>
        See Post
        <img src="../assets/logo.png" class="button-icon" alt="button logo" />
      </button>
    </a>
  </main>
</template>

<script>
export default {
  name: "Post",

  props: ["title", "description", "link"]
};
</script>

<style>
.post {
  text-align: center;
  box-shadow: 0px 3px 7px 3px grey;
  padding: 10px;
}
.post__description {
  font-size: 2rem;
}
.post__link {
  font-size: 1.5rem;
}

.post__link button {
  height: 50px;
  width: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
	margin: 0 auto;
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