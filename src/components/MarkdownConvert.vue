<script setup>
import { marked } from 'marked'
import { onMounted } from 'vue'
import { computed, ref, watch } from 'vue'
const props = defineProps({
  path: {
    type: String,
    required: true
  }
})
const { path } = props

const htmlContent = ref('')
onMounted(async () => {
  const response = await fetch(path)
  const data = await response.text()
  htmlContent.value = marked(data)
})
</script>
<template>
  <div v-html="htmlContent"></div>
</template>
