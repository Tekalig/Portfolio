<template>
  <div id="app" class="font-sans bg-gray-100 text-black min-h-screen flex dark:bg-gray-900 dark:text-white">
    <!-- Left Sidebar -->
    <Sidebar class="w-1/4 hidden md:block" />

    <!-- Main Content Area -->
    <div class="flex-1 flex flex-col items-center justify-center min-h-screen">
      <router-view />
    </div>

    <!-- Right Sidebar -->
    <ProfileCard class="w-1/4 hidden md:block" />
  </div>

  <!-- Footer -->
  <Footer class="w-full" />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Footer from './components/Footer.vue';
import Sidebar from './components/Sidebar.vue';
import ProfileCard from './components/ProfileCard.vue';

export default defineComponent({
  components: { Footer, Sidebar, ProfileCard },
});
</script>
