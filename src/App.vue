<script setup lang="ts">
useHead({
  title: import.meta.env.VITE_APP_TITLE,
})
</script>

<template>
  <main font-sans p="x-4 y-10">
    <RouterView />
  </main>
</template>
