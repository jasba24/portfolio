<template>
  <div class="about">
    <Profile></Profile>
  </div>
</template>

<script>
import Profile from "@/components/PfProfile";

export default {
  name: "About",
  components: { Profile }
};
</script>

<style>
.about {
  display: flex;
  height: calc(100vh - 150px);
  flex-direction: column;
  align-content: center;
  justify-content: center;
}
</style>