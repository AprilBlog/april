<script lang="ts" setup>
const { t } = useI18n()
</script>

<template>
  <!-- TODO: make editor better -->

  <div class="flex flex-col items-center">
    <!-- FIXME: How to use vue-i18n in html attribute? -->
    <input
      id="title"
      type="text"
      autofocus="true"
      placeholder="Title"
      class="bg-transparent text-4xl mb-5 text-gray-500"
      style="width:80%;"
    >
  </div>
</template>

<style>
@import url(vditor/dist/index.css);

#title:focus{
  outline: none;
}
</style>

<route lang="yaml">
meta:
  layout: default
</route>
