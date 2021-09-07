<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <div>{{ t("pong") }}</div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
