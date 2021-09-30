<template>
  <h1 class="posts__title">Posts</h1>
  <template class="posts__container">
    <Post
      v-for="(p, i) in posts"
      :key="i"
      :title="p.title"
      :description="p.description"
      :link="p.link"
      :urlLink="p.urlLink"
      :time="p.time"
    ></Post>
  </template>
</template>

<script setup>
import Post from "@/components/PfPost"
import { ref } from "vue"

const posts = ref([
  {
    title: "Como añadir un nuevo usuario root en mysql-workbench",
    description:
      "Para crear un nuevo usuario usa estos comandos: Primero abre mysql con sudo en tu terminal lo cual les pedira la contraseña del computador y le abrira esta interfaz en la consola",
    time: "June, 2021  2 minutos",
    link:
      "https://dev.to/jasba24/como-anadir-un-nuevo-usuario-root-en-mysql-workbench-59gc",
  },
  {
    title: "Como enviar un proceso en la terminal a un segundo plano",
    description:
      "Probablemente cuando has iniciado un proyecto corres en tu terminal: \n npm run start lo cual te abre un servidor para poder desarrollar en local pero si necesitabas instalar una nueva librería tenias que matar tu servidor e instalarla y volver a iniciar el servidor.",
    time: "April, 2021  1 minuto",
    link:
      "https://dev.to/jasba24/como-enviar-un-proceso-en-la-terminal-a-un-segundo-plano-31ip",
  },
])
</script>
