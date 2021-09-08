<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <Card class="w-100 h-auto bg-white flex items-center content-center flow-root p-8">
    <h1 class="text-size-4xl font-serif text-left pb-6">
      {{ t("login.title") }}
    </h1>
    <Metamask />
  </Card>
</template>
