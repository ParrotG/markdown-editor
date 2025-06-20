<template>
  <div class="prose prose-slate max-w-none" v-html="compiledHtml" />
</template>

<script lang="ts" setup>
import { computed } from 'vue'
import MarkdownIt from 'markdown-it'

// Props
const props = withDefaults(
    defineProps<{
      content?: string
    }>(),
    {
      content: ''
    }
)


// 实例化 MarkdownIt
const md = new MarkdownIt({
  html: true,
  linkify: true,
  typographer: true
})

// 计算后的 HTML 内容
const compiledHtml = computed(() => md.render(props.content))

</script>

<style scoped>
/* 可选：Tailwind Typography 插件增强 markdown 样式 */
</style>
