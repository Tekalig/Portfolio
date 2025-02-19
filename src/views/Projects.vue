<template>
    <div class="pt-24 px-6">
        <h1 class="text-5xl font-bold text-purple-400">My Projects</h1>
        <div class="mt-8 space-y-6">
            <div class="p-6 bg-gray-800 rounded-lg shadow-lg">
                <h2 class="text-2xl font-semibold text-purple-400">Project 1</h2>
                <p class="mt-2 text-gray-300">
                    A modern web application built with Vue.js and Tailwind CSS.
                </p>
                <a href="https://github.com/yourusername/project1" class="mt-4 inline-block text-purple-400 hover:underline">
                    <font-awesome-icon :icon="['fab', 'github']" /> View Project
                </a>
            </div>
            <div class="p-6 bg-gray-800 rounded-lg shadow-lg">
                <h2 class="text-2xl font-semibold text-purple-400">Project 2</h2>
                <p class="mt-2 text-gray-300">
                    A REST API built with Node.js and Express.
                </p>
                <a href="https://github.com/yourusername/project2" class="mt-4 inline-block text-purple-400 hover:underline">
                    <font-awesome-icon :icon="['fab', 'github']" /> View Project
                </a>
            </div>
            <div class="p-6 bg-gray-800 rounded-lg shadow-lg">
                <h2 class="text-2xl font-semibold text-purple-400">Project 3</h2>
                <p class="mt-2 text-gray-300">
                    A mobile app built with React Native.
                </p>
                <a href="https://github.com/yourusername/project3" class="mt-4 inline-block text-purple-400 hover:underline">
                    <font-awesome-icon :icon="['fab', 'github']" /> View Project
                </a>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

export default defineComponent({
    name: 'Projects',
    components: {
        FontAwesomeIcon,
    },
});
</script>

<style scoped>
/* Add your styles here */
</style>