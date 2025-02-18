<template>
    <div class="flex items-center justify-center h-screen bg-gray-100 dark:bg-gray-900 px-6">
        <div class="max-w-4xl text-center flex flex-col md:flex-row items-center gap-8">
            <!-- Text Section -->
            <div class="text-left">
                <h1 class="text-4xl font-bold text-gray-900 dark:text-white">
                    I’m <span class="text-yellow-500">Rayan Adlrdard</span>
                </h1>
                <h2 class="text-3xl font-bold text-gray-700 dark:text-gray-300 mt-2">
                    Front-end Developer
                </h2>
                <p class="text-gray-600 dark:text-gray-400 mt-4">
                    Lorem Ipsum Dolor Sit Amet, Consectetur Adipiscing Elit. Et, Volutpat Feugiat
                    Placerat Lobortis. Natoque Rutrum Semper Sed Suspendisse Nunc Lectus.
                </p>
                <button
                    class="mt-6 px-6 py-3 bg-yellow-500 text-white font-bold rounded-lg shadow-md hover:bg-yellow-600">
                    HIRE ME →
                </button>
            </div>
            <!-- Image Section -->
            <div class="flex-shrink-0">
                <img src="../assets/images/profile.jpg" alt="Profile" class="w-64 h-64 rounded-lg shadow-lg" />
            </div>
        </div>
        
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
    name: "HeroSection"
});
</script>

<style>
@import "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css";
</style>