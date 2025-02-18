<template>
    <div class="flex flex-col items-center justify-center bg-gray-100 dark:bg-gray-900 px-6"> 
        <HeroSection />
        <ServicesSection />
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ServicesSection from "../components/ServicesSection.vue";
import HeroSection from "../components/HeroSection.vue";

export default defineComponent({
    name: "Home",
    components: {ServicesSection, HeroSection}
});
</script>

<style>
@import "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css";
</style>
