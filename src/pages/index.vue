<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <!-- TODO: editor-->
  <div class="text-center my-auto">
    {{ t("pong") }}
  </div>
</template>

<route lang="yaml">
meta:
  layout: default
</route>
