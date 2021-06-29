<template>
  <h1 class="posts__title">Blog posts</h1>
  <template class="posts__container">
    <Post
      v-for="(p, i) in posts"
      :key="i"
      :title="p.title"
      :description="p.description"
      :link="p.link"
      :urlLink="p.urlLink"
    ></Post>
  </template>
</template>

<script>
import Post from "@/components/PfPost";

export default {
  name: "Posts",

  components: { Post },

  data() {
    return {
      posts: [
        {
          title: "Como añadir un nuevo usuario root en mysql-workbench",
          description:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Perspiciatis, fugit delectus nostrum facilis quidem vero cupiditate odio.",
          link: "https://dev.to/jasba24/como-anadir-un-nuevo-usuario-root-en-mysql-workbench-59gc"
        },
        {
          title: "Como enviar un proceso en la terminal a un segundo plano",
          description:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Perspiciatis, fugit delectus nostrum facilis quidem vero cupiditate odio.",
          link: "https://dev.to/jasba24/como-enviar-un-proceso-en-la-terminal-a-un-segundo-plano-31ip"
        }
      ]
    };
  }
};
</script>

<style>
.posts__title {
  text-align: center;
  margin: 20px 0;
}
.posts__container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: calc(100% - 40px);
  margin: 0 20px;
}
</style>