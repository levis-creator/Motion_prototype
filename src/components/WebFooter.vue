<script setup>
import logo from '@/assets/MotionLogo.png'
import { menu_items } from '../lib/static'
import { RouterLink } from 'vue-router'
import { Icon } from '@iconify/vue'
</script>
<template>
  <footer class="lg:px-28 py-9">
    <div class="flex flex-col gap-3 mb-4 sm:flex-row sm:items-center sm:justify-between">
      <div>
        <img :src="logo" alt="Motion Logo" class="w-auto h-10" />
      </div>
      <ul class="pl-3 sm:flex sm:flex-row sm:gap-4">
        <li v-for="(item, i) in menu_items" :key="i">
          <RouterLink :to="item.path" class="block font-semibold text-gray-700 hover:text-gray-900">
            {{ item.title }}
          </RouterLink>
        </li>
      </ul>
      <!-- social links -->
      <ul class="flex gap-3 px-3 text-gray-800">
        <li>
          <Icon icon="fa6-brands:facebook" height="26" />
        </li>
        <li>
          <Icon icon="fa6-brands:instagram" height="26" />
        </li>
        <li>
          <Icon icon="fa6-brands:x-twitter" height="26" />
        </li>
        <li>
          <Icon icon="fa6-brands:linkedin" height="26" />
        </li>
        <li>
          <Icon icon="fa6-brands:youtube" height="26" />
        </li>
      </ul>
    </div>
    <hr />
    <div class="text-center">
      <p>
        &copy; 2022 Motion. All rights reserved. Designed by
        <a href="https://www.levisnyingi.tech/" target="_blank">Levis Nyingi</a>
      </p>
    </div>
  </footer>
</template>
