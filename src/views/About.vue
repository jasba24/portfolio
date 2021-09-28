<template>
  <div class="about">
    <Profile></Profile>
  </div>
</template>

<script setup>
import Profile from "@/components/PfProfile"
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
