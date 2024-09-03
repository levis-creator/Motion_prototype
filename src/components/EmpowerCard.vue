<script setup>
const props = defineProps({
  data: {
    type: Object,
    required: true
  }
})

const { data } = props
</script>
<template>
  <div class="mb-8 space-y-4 text-gray-800">
    <div class="p-3 bg-blue-700 rounded-xl w-fit">
      <img :src="data.icon" class="w-full h-full" />
    </div>
    <div class="space-y-4">
      <h3 class="mb-2 text-3xl font-semibold">{{ data.title }}</h3>
      <p>{{ data.description }}</p>
    </div>
  </div>
</template>
