<template>
  <nav class="p-6 bg-gray-800 fixed w-full top-0 z-50">
    <div class="container mx-auto flex justify-between items-center">
      <router-link to="/" class="text-2xl font-bold text-purple-400">My Portfolio</router-link>
      <div class="hidden md:flex space-x-4">
        <router-link to="/" class="hover:text-purple-400">Home</router-link>
        <router-link to="/about" class="hover:text-purple-400">About</router-link>
        <router-link to="/projects" class="hover:text-purple-400">Projects</router-link>
        <router-link to="/contact" class="hover:text-purple-400">Contact</router-link>
      </div>
      <button @click="toggleMenu" class="md:hidden text-purple-400">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
        </svg>
      </button>
    </div>
    <div v-if="isMenuOpen" class="md:hidden mt-4 space-y-2">
      <router-link to="/" class="block hover:text-purple-400">Home</router-link>
      <router-link to="/about" class="block hover:text-purple-400">About</router-link>
      <router-link to="/projects" class="block hover:text-purple-400">Projects</router-link>
      <router-link to="/contact" class="block hover:text-purple-400">Contact</router-link>
    </div>
  </nav>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'Navbar',
  setup() {
    const isMenuOpen = ref(false);
    const toggleMenu = () => {
      isMenuOpen.value = !isMenuOpen.value;
    };
    return { isMenuOpen, toggleMenu };
  },
});
</script>

<style scoped>
nav {
  transition: background-color 0.3s ease;
}
nav:hover {
  background-color: #4a5568;
}
</style>