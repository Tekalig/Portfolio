<template>
  <div id="app" class="font-sans bg-gray-50 text-black min-h-screen flex dark:bg-gray-900 dark:text-white">
    <!-- Left Sidebar -->
    <Sidebar class="w-1/5 hidden md:block" />

    <!-- Main Content Area -->
    <div class="flex-1 flex flex-col items-center justify-center min-h-screen">
      <router-view />
    </div>

    <!-- Right Sidebar -->
    <ProfieCard class="w-1/5 hidden md:block" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Footer from './components/Footer.vue';
import Sidebar from './components/Sidebar.vue';
import ProfieCard from './components/Profile-card.vue';

export default defineComponent({
  components: { Footer, Sidebar, ProfieCard },
});
</script>

<style scoped>
/* Add styles if necessary */
</style>
