<script setup lang="ts">
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
      enable: true,
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
  <div id="vditor"></div>
</template>

<style>
.vditor {
  border: unset!important;
}
.vditor-toolbar {
  border-bottom: unset!important;
}
</style>
