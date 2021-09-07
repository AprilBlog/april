<script setup lang="ts">
const { t, availableLocales, locale } = useI18n()

const toggleLocales = () => {
  // change to some real logic
  const locales = availableLocales
  locale.value = locales[(locales.indexOf(locale.value) + 1) % locales.length]
}
</script>

<template>
  <header class="flex justify-between py-6">
    <router-link class="text-4xl" to="/" :title="t('header.title')">
      {{ t("header.title") }}
    </router-link>

    <div class="flex items-end space-x-5">
      <Avatar :title="t('header.avatar')" />

      <a :title="t('header.toggle_langs')" @click="toggleLocales">
        <carbon-language />
      </a>

      <router-link to="/about" :title="t('header.about')">
        <carbon-dicom-overlay />
      </router-link>
    </div>
  </header>
</template>
