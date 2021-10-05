<script setup lang="ts">
// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
useHead({
  title: 'April',
  meta: [
    { name: 'description', content: ' A Blog Platform runs on the top of RSS3' },
  ],
})
</script>

<template>
  <router-view />
</template>
