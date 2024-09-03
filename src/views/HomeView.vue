<script setup>
import MarkdownConvert from '@/components/MarkdownConvert.vue'
import innovate from '@/assets/Innovation.png'
import discover from '@/assets/Discover.png'
import EmpowerCard from '@/components/EmpowerCard.vue'
import { empower_info } from '@/lib/static'
import efficiency from '@/assets/Efficiency.png'
</script>

<template>
  <main class="py-3 pt-24">
    <section class="space-y-4 lg:mx-40">
      <!-- Hero text -->
      <div
        class="hero-container [&_h6]:text-blue-700 <!-- h6 --> [&_h6]:font-semibold text-center [&_h6]:text-base <!-- h1 --> [&_h1]:font-extrabold [&_h1]:text-3xl [&_h1]:md:text-5xl [&_h1]:lg:text-6xl [&_h1]:lg:my-6 [&_h1]:my-3 [&_h1]:md:my-5 [&_p]:text-lg [&_p]:text-gray-800"
      >
        <MarkdownConvert path="/content/HeroText.md" />
      </div>
      <!-- group buttons -->
      <div className="flex gap-3 justify-center w-full">
        <button class="p-2 px-4 text-white bg-blue-700 rounded-md">Get Started</button>
        <button class="p-2 px-4 font-semibold text-blue-700 border-2 border-blue-700 rounded-md">
          Contact us
        </button>
      </div>
      <!-- list items -->
      <div
        class="[&_ul]:flex [&_ul]:justify-center [&_ul]:flex-wrap [&_ul]:gap-3 [&_li]:before:content-['✓'] [&_li]:before:w-[2em] [&_li]:before:h-[2em] [&_li]:before:text-green-600 [&_li]:before:mr-1 [&_li]:before:font-bold"
      >
        <MarkdownConvert path="/content/HeroList.md" />
      </div>
    </section>
    <!-- innovation -->
    <section class="mt-44 my-36 lg:mx-28">
      <div class="md:flex md:gap-5 lg:gap-16">
        <div class="overflow-hidden md:basis-1/2 rounded-2xl">
          <img :src="innovate" alt="innovation intro" class="object-cover w-full h-full" />
        </div>
        <div class="md:basis-1/2">
          <div
            class="[&_h6]:font-semibold [&_h6]:text-base [&_h6]:md:text-2xl [&_h6]:text-blue-700 [&_h2]:font-bold [&_h2]:text-3xl [&_h2]:lg:mt-3 [&_h2]:lg:my-6 [&_h2]:my-3 [&_h2]:md:my-5 [&_p]:text-lg text-gray-800 [&_table]:my-5 [&_thead]:text-left"
          >
            <MarkdownConvert path="/content/InnovationText.md" />
          </div>
          <button class="p-2 px-4 text-white bg-blue-700 rounded-md">Get Started</button>
        </div>
      </div>
    </section>
    <!-- discover -->
    <section class="py-10 mt-44 my-36 lg:px-28 bg-gray-50">
      <div class="md:flex md:gap-5 lg:gap-16">
        <div class="md:basis-1/2">
          <div
            class="[&_h6]:font-semibold [&_h6]:text-base [&_h6]:md:text-2xl [&_h6]:text-blue-700 [&_h2]:font-bold [&_h2]:text-3xl [&_h2]:lg:mt-3 [&_h2]:lg:my-6 [&_h2]:my-3 [&_h2]:md:my-5 [&_p]:text-lg text-gray-800 [&_table]:my-5 [&_thead]:text-left"
          >
            <MarkdownConvert path="/content/Discover.md" />
          </div>
          <button class="p-2 px-4 text-white bg-blue-700 rounded-md">Get Started</button>
        </div>
        <div class="overflow-hidden md:basis-1/2 rounded-2xl">
          <img :src="discover" alt="innovation intro" class="object-cover w-full h-full" />
        </div>
      </div>
    </section>
    <!-- Empower -->
    <section class="mt-44 my-36 lg:mx-28">
      <div class="flex flex-col gap-8 lg:flex-row lg:gap-12">
        <div class="lg:basis-2/4">
          <div
            class="[&_h6]:font-semibold [&_h6]:text-base [&_h6]:md:text-2xl [&_h6]:text-blue-700 [&_h2]:font-extrabold [&_h2]:text-3xl [&_h2]:lg:text-3xl [&_h2]:lg:mt-3 [&_h2]:lg:my-6 [&_h2]:my-3 [&_h2]:md:my-5 [&_p]:text-lg text-gray-800 mb-5"
          >
            <MarkdownConvert path="/content/Empower.md" />
          </div>
          <button class="p-2 px-4 text-white bg-blue-700 rounded-md">Get Started</button>
        </div>
        <div class="grid flex-grow grid-cols-1 sm:grid-cols-2 gap-x-8">
          <EmpowerCard v-for="(empower, i) in empower_info" :key="i" :data="empower" />
        </div>
      </div>
    </section>
    <!-- Efficient -->
    <section class="py-10 lg:px-28 bg-gray-50">
      <div class="md:flex md:gap-5 lg:gap-16">
        <div class="overflow-hidden md:basis-1/2 rounded-2xl">
          <img :src="efficiency" alt="innovation intro" class="object-cover w-full h-full" />
        </div>
        <div class="md:basis-1/2">
          <div
            class="[&_h6]:font-semibold [&_h6]:text-base [&_h6]:md:text-2xl [&_h6]:text-blue-700 [&_h2]:font-bold [&_h2]:text-3xl [&_h2]:lg:mt-3 [&_h2]:lg:my-6 [&_h2]:my-3 [&_h2]:md:my-5 [&_p]:text-lg text-gray-800 [&_table]:my-5 [&_thead]:text-left"
          >
            <MarkdownConvert path="/content/InnovationText.md" />
          </div>
          <button class="p-2 px-4 text-white bg-blue-700 rounded-md">Get Started</button>
        </div>
      </div>
    </section>
    <div
      class="[&_h6]:font-semibold [&_h6]:text-base [&_h6]:md:text-2xl [&_h6]:text-blue-700 [&_h2]:font-bold [&_h2]:text-3xl [&_h2]:lg:mt-3 [&_h2]:lg:my-6 [&_h2]:my-3 [&_h2]:md:my-5 [&_p]:text-lg text-gray-800 [&_table]:my-5 [&_thead]:text-left py-10 lg:px-28 flex flex-col gap-6 md:flex-row justify-between items-center"
    >
      <div>
        <h2>Discover Motion's Powerful Business Solutions</h2>
        <p>Unlock your business potential with Motion's innovative solutions</p>
      </div>
      <div className="flex gap-3 justify-center ">
        <button class="p-2 px-4 text-white bg-blue-700 rounded-md h-fit">Get Started</button>
        <button
          class="p-2 px-4 font-semibold text-blue-700 border-2 border-blue-700 rounded-md h-fit"
        >
          Contact us
        </button>
      </div>
    </div>
  </main>
</template>
