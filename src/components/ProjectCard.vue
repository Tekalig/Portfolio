<template>
  <div
    class="bg-gray-100 dark:bg-gray-800 rounded-2xl overflow-hidden shadow-lg hover:shadow-2xl transition-shadow duration-300">
    <img :src="image" alt="Project Image" class="w-full h-48 object-cover" />
    <div class="p-6">
      <h3 class="text-2xl font-semibold mb-2 text-white">{{ title }}</h3>
      <p class="text-gray-400 mb-4">{{ description }}</p>
      <span class="text-sm text-purple-400 block mb-4">{{ tech }}</span>
      <div class="flex gap-4">
        <a v-if="liveLink" :href="liveLink"
          class="bg-yellow-500 dark:bg-green-500 hover:bg-yellow-700 text-white py-2 px-4 rounded-full transition-colors duration-300"
          target="_blank">Live ↔️</a>
        <a v-if="cachedLink" :href="cachedLink"
          class="bg-yellow-500 dark:bg-green-500 dark:hover:dark:bg-green-600 hover:bg-yellow-600 text-white py-2 px-4 rounded-full transition-colors duration-300"
          target="_blank">Cached ➤</a>
        <a v-if="githubLink" :href="githubLink"
          class="bg-yellow-500 dark:bg-green-500 dark:hover:dark:bg-green-600 hover:bg-yellow-600 text-white py-2 px-4 rounded-full transition-colors duration-300"
          target="_blank">GitHub ↔️</a>
        <a v-if="figmaLink" :href="figmaLink"
          class="bg-yellow-500 dark:bg-green-500 dark:hover:dark:bg-green-600 hover:bg-yellow-600 text-white py-2 px-4 rounded-full transition-colors duration-300"
          target="_blank">Figma ➤</a>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

defineProps({
  title: String,
  description: String,
  tech: String,
  liveLink: String,
  cachedLink: String,
  githubLink: String,
  figmaLink: String,
  image: String,
});
</script>
