<template>
    <div class="flex flex-row h-screen fixed">
        <!-- Sidebar -->
        <div class="w-28 bg-gray-100 dark:bg-gray-800 flex flex-col items-center py-4 h-full">
            <div class="flex flex-col space-y-6 flex-1">
                <router-link to="/" class="flex flex-col items-center">
                    <div class="p-2 rounded bg-gray-200 dark:bg-gray-700" :class="{'bg-yellow-500 text-white': isActive('/')}" @click="setActive('/')">
                        <font-awesome-icon :icon="['fas', 'home']"></font-awesome-icon>
                    </div>
                    <p class="text-xs mt-1">Home</p>
                </router-link>
                <router-link to="/projects" class="flex flex-col items-center">
                    <div class="p-2 rounded bg-gray-200 dark:bg-gray-700" :class="{'bg-yellow-500 text-white': isActive('/projects')}" @click="setActive('/projects')">
                        <font-awesome-icon :icon="['fas', 'file-alt']"></font-awesome-icon>
                    </div>
                    <p class="text-xs mt-1">Projects</p>
                </router-link>
                <router-link to="/education" class="flex flex-col items-center">
                    <div class="p-2 rounded bg-gray-200 dark:bg-gray-700" :class="{'bg-yellow-500 text-white': isActive('/education')}" @click="setActive('/education')">
                        <font-awesome-icon :icon="['fas', 'user-graduate']"></font-awesome-icon>
                    </div>
                    <p class="text-xs mt-1">Education</p>
                </router-link>
                <router-link to="/work" class="flex flex-col items-center">
                    <div class="p-2 rounded bg-gray-200 dark:bg-gray-700" :class="{'bg-yellow-500 text-white': isActive('/work')}" @click="setActive('/work')">
                        <font-awesome-icon :icon="['fas', 'briefcase']"></font-awesome-icon>
                    </div>
                    <p class="text-xs mt-1">Work</p>
                </router-link>
                <router-link to="/design" class="flex flex-col items-center">
                    <div class="p-2 rounded bg-gray-200 dark:bg-gray-700" :class="{'bg-yellow-500 text-white': isActive('/design')}" @click="setActive('/design')">
                        <font-awesome-icon :icon="['fas', 'paint-brush']"></font-awesome-icon>
                    </div>
                    <p class="text-xs mt-1">Design</p>
                </router-link>
                <router-link to="/contact" class="flex flex-col items-center">
                    <div class="p-2 rounded bg-gray-200 dark:bg-gray-700" :class="{'bg-yellow-500 text-white': isActive('/contact')}" @click="setActive('/contact')">
                        <font-awesome-icon :icon="['fas', 'comment']"></font-awesome-icon>
                    </div>
                    <p class="text-xs mt-1">Contact</p>
                </router-link>
            </div>
            <!-- Dark Mode Toggle -->
            <button @click="toggleDarkMode" 
                    class="flex flex-col items-center p-2 rounded mb-4"
                    :class="darkMode ? 'bg-gray-600' : 'bg-gray-300'">
                <font-awesome-icon :icon="darkMode ? ['fas', 'moon'] : ['fas', 'sun']"></font-awesome-icon>
            </button>
        </div>
        <!-- Main Content -->
        <div class="flex-1 p-6 ml-28">
            <slot></slot>
        </div>
    </div>
</template>

<script lang="ts">
import { library } from '@fortawesome/fontawesome-svg-core';
import { faHome, faFileAlt, faUserGraduate, faBriefcase, faPaintBrush, faComment, faMoon, faSun } from '@fortawesome/free-solid-svg-icons';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { defineComponent } from 'vue';

library.add(faHome, faFileAlt, faUserGraduate, faBriefcase, faPaintBrush, faComment, faMoon, faSun);

export default defineComponent({
    name: 'Sidebar',
    components: {
        FontAwesomeIcon
    },
    data() {
        return {
            darkMode: false,
            activeRoute: '/'
        };
    },
    methods: {
        toggleDarkMode() {
            this.darkMode = !this.darkMode;
            if (this.darkMode) {
                document.documentElement.classList.add('dark');
            } else {
                document.documentElement.classList.remove('dark');
            }
        },
        setActive(route: string) {
            this.activeRoute = route;
        },
        isActive(route: string) {
            return this.activeRoute === route;
        }
    },
});
</script>

<style>
@import "animate.css/animate.min.css";
</style>
