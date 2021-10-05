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
  <router-link to="/post" :title="t('header.post')">
    <button border="1px solid [#282828]" class="rounded-10px w-20 h-10 text-xl font-serif">
      {{ t("header.post") }}
    </button>
  </router-link>
</template>
