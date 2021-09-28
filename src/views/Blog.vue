<template>
  <div class="blog">
    <Posts></Posts>
  </div>
</template>

<script>
import Posts from "@/components/PfPosts"

export default {
  name: "blog",
  components: { Posts },
}
</script>

<style>
.blog {
  display: flex;
  height: calc(100vh - 150px);
  flex-direction: column;
  align-content: center;
  justify-content: center;
}
</style>
