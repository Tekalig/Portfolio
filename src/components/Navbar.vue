<template>
  <nav class="p-6 bg-gray-800 fixed w-full top-0 z-50">
    <div class="container mx-auto flex justify-between items-center">
      <router-link to="/" class="text-2xl font-bold text-purple-400">My Portfolio</router-link>
      <div class="space-x-4">
        <router-link to="/" class="hover:text-purple-400">Home</router-link>
        <router-link to="/about" class="hover:text-purple-400">About</router-link>
        <router-link to="/projects" class="hover:text-purple-400">Projects</router-link>
        <router-link to="/contact" class="hover:text-purple-400">Contact</router-link>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Navbar',
});
</script>