<template>
  <main class="post">
    <h1 class="post__title">{{ title }}</h1>
    <p class="post__description">{{ description }}</p>
    <a class="post__link" :href="link" target="_blank">
      <button>
        See Post
      </button>
    </a>
  </main>
</template>

<script setup>
defineProps(["title", "description", "link"])
</script>

<style>
.post {
  width: 30%;
  text-align: center;
  box-shadow: 0px 3px 7px 3px var(--primary-color);
  padding: 10px;
  margin-right: 20px;
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
  color: white;
  font-weight: bold;
  font-size: 2.5rem;
  background-color: var(--primary-color);
  color: #ffc069;
}
</style>
