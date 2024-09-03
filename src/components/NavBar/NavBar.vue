<script setup>
import { ref } from 'vue'
import { Icon } from '@iconify/vue'
import MenuList from './MenuList.vue'
import logo from '@/assets/MotionLogo.png'
let openMenu = ref(false)

const toggleMenu = () => {
  openMenu.value = !openMenu.value
}
</script>

<template>
  <nav
    class="sticky top-0 z-10 flex items-center w-full px-3 py-3 bg-white border-b-2 border-b-gray-300 md:px-8"
  >
    <MenuList className="hidden font-bold! text-gray-800" />
    <!-- logo -->
    <div class="flex-grow text-xl sm:text-center">
      <img :src="logo" alt="Motion Logo" class="mx-auto" />
    </div>
    <!-- Toggle button -->
    <button class="sm:hidden" @click="toggleMenu">
      <Icon icon="material-symbols:close-rounded" height="25" v-if="openMenu" />
      <Icon icon="material-symbols:menu" height="25" v-else />
    </button>
    <!-- group buttons -->
    <div className="sm:flex gap-3 hidden">
      <button class="p-2 px-4 font-semibold text-blue-700 border-2 border-blue-700 rounded-md">
        Get Started
      </button>
      <button class="p-2 px-4 text-white bg-blue-700 rounded-md">Login</button>
    </div>
  </nav>
  <!-- pop menu -->
  <div class="left-0 right-0 px-3 py-2 shadow-" v-if="openMenu" @mouseout="toggleMenu">
    <MenuList />
  </div>
</template>
