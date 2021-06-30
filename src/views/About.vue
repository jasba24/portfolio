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
  background: radial-gradient(
      50% 50% at 50% 50%,
      rgba(26, 21, 21, 0) 0%,
      rgba(1, 1, 1, 0.16) 100%
    ),
    #ffffff;
}
</style>