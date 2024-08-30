<script setup>
import { computed } from 'vue'
import { menu_items } from '../../lib/static'
const props = defineProps({
  className: { type: String, required: false }
})

const { className } = props

const computedClass = computed(() => `gap-2 font-semibold  sm:flex ${className}`)
</script>
<template>
  <ul :class="computedClass">
    <li v-for="(item, i) in menu_items" :key="i">
      <RouterLink :to="item.path" class="hover:text-blue-700">
        {{ item.title }}
      </RouterLink>
    </li>
  </ul>
</template>
