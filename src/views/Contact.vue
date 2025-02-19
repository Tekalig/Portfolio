<template>
    <div class="px-6">
        <h1 class="text-5xl font-bold text-purple-400">Contact Me</h1>
        <p class="mt-4 text-gray-300">
            Feel free to reach out to me for collaborations, job opportunities, or just to say hi!
        </p>
        <form class="mt-8 space-y-6">
            <div>
                <label for="name" class="block text-gray-300">Name</label>
                <input type="text" id="name"
                    class="mt-2 p-2 w-full bg-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-400"
                    placeholder="Your Name" />
            </div>
            <div>
                <label for="email" class="block text-gray-300">Email</label>
                <input type="email" id="email"
                    class="mt-2 p-2 w-full bg-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-400"
                    placeholder="Your Email" />
            </div>
            <div>
                <label for="message" class="block text-gray-300">Message</label>
                <textarea id="message"
                    class="mt-2 p-2 w-full bg-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-400"
                    rows="4" placeholder="Your Message"></textarea>
            </div>
            <button type="submit"
                class="px-6 py-2 bg-purple-400 text-white rounded-lg hover:bg-purple-500 transition-colors">
                Send Message
            </button>
        </form>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'Contact',
});
</script>

<style scoped>
/* Add your styles here */
</style>