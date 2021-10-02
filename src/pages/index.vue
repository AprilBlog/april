<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <div class="pb-6 text-center">
    {{ t("pong") }}
  </div>
  <div class="flex justify-center">
    <Login />
  </div>
</template>

<route lang="yaml">
meta:
  layout: default
</route>
