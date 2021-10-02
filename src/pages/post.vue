<script lang="ts" setup>
import { onMounted } from 'vue'
import Vditor from 'vditor'

const initVditor = () => {
  const vditor = new Vditor('vditor', {
    height: 360,
    width: '60%',
    toolbarConfig: {
      pin: true,
    },
    cache: {
      enable: false,
    },
    after: () => {
    },
  })
}

onMounted(() => {
  initVditor()
})
</script>

<template>
  <!-- TODO: make editor better -->
  <div class="flex justify-center">
    <div id="vditor"></div>
  </div>
</template>

<style>
@import url(vditor/dist/index.css);
</style>

<route lang="yaml">
meta:
  layout: default
</route>
