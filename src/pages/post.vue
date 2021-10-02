<script lang="ts" setup>
import { onMounted } from 'vue'
import Vditor from 'vditor'

const initVditor = () => {
  const vditor = new Vditor('vditor', {
    mode: 'wysiwyg',
    icon: 'material',
    height: 480,
    width: '80%',
    counter: {
      enable: true,
    },
    toolbar: ['headings', 'bold', 'italic', 'strike', 'link', '|',
      'list', 'ordered-list', 'check', '|',
      'quote', 'line', 'code', 'inline-code', '|',
      'upload', 'record', 'table',
    ],
    toolbarConfig: {
      pin: true,
    },
    preview: {
      actions: [],
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

.vditor {
  border: unset!important;
}
.vditor-toolbar {
  border-bottom: unset!important;
}
</style>

<route lang="yaml">
meta:
  layout: default
</route>
