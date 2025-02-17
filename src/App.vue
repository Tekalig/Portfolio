<template>
  <div id="app" class="font-sans bg-gray-900 text-white min-h-screen">
    <Navbar />
    <router-view />
    <Footer />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

export default defineComponent({
  components: { Navbar, Footer },
});
</script>