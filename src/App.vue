<template>
  <div class="max-w-prose mx-auto px-4 sm:px-6">
      <MarkdownViewer :content="markdownSource" />
  </div>

</template>

<script setup lang="ts">
import MarkdownViewer from './components/MarkdownViewer.vue'

const markdownSource = `
`
</script>

<style scoped>

</style>