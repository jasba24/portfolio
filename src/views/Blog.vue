<template>
  <div class="blog">
    <Posts></Posts>
  </div>
</template>

<script>
import Posts from "@/components/PfPosts";

export default {
  name: "blog",
  components: { Posts },
};
</script>