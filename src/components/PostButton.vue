<script lang="ts" setup>
const { t } = useI18n()
</script>

<template>
  <router-link to="/post" :title="t('header.edit')">
    <button border="1px solid [#282828]" class="rounded-10px w-20 h-10 text-xl font-serif">
      {{ t("header.post") }}
    </button>
  </router-link>
</template>
