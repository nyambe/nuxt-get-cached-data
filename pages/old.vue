<script setup lang="ts">
const nuxtApp = useNuxtApp()
const { data } = await useFetch<any>('https://icanhazdadjoke.com/', {
  headers: {
    Accept: 'application/json'
  },
})
</script>

<template>
  <div>
    <h1>Fetch Antiguo</h1>
    {{ data.joke }}
    <NuxtLink to="/about">To the about page</NuxtLink>
  </div>
</template>