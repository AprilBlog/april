/* eslint-disable vue/no-parsing-error */
/* eslint-disable vue/no-parsing-error */
<script lang="ts" setup>
import { onMounted } from 'vue'
import Vditor from 'vditor'
const { t } = useI18n()

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
    <div id="vditor"></div>
  </div>
</template>

<style>
@import url(vditor/dist/index.css);

#title:focus{
  outline: none;
}
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
