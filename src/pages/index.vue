<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <!-- TODO: editor-->
  <div class="pb-6">
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
