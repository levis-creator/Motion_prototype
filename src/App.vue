<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavBar from '@/components/NavBar/NavBar.vue'
import WebFooter from '@/components/WebFooter.vue'
</script>

<template>
  <NavBar />
  <RouterView />
  <WebFooter />
</template>
