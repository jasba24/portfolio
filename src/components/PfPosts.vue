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
          title: "Lorem ipsum",
          description:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Perspiciatis, fugit delectus nostrum facilis quidem vero cupiditate odio deserunt ut in, maiores similique est modi. Natus obcaecati blanditiis architecto excepturi rerum.",
          link: "https://twitter.com/jasba24"
        },
        {
          title: "Lorem ipsum",
          description:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Perspiciatis, fugit delectus nostrum facilis quidem vero cupiditate odio deserunt ut in, maiores similique est modi. Natus obcaecati blanditiis architecto excepturi rerum.",
          link: "https://twitter.com/jasba24"
        },
        {
          title: "Lorem ipsum",
          description:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Perspiciatis, fugit delectus nostrum facilis quidem vero cupiditate odio deserunt ut in, maiores similique est modi. Natus obcaecati blanditiis architecto excepturi rerum.",
          link: "https://twitter.com/jasba24"
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
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  margin: 0 20px;
}
</style>