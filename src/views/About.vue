<template>
  <div class="about">
    <Profile></Profile>
  </div>
</template>

<script>
import Profile from "@/components/PfProfile";

export default {
  name: "About",
  components: { Profile },
};
</script>

<style>
.footer.bottom {
  position: absolute;
  bottom: 0;
  width: 100%;
}
</style>