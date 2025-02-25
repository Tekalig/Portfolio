<template>
    <div class="flex flex-col md:flex-row gap-4 max-w-5xl">
        <!-- Contact Information -->
        <div class="md:w-1/2 dark:text-white p-4">
            <h2 class="text-3xl font-bold mb-4 dark:text-white">Contact Information</h2>
            <div class=" shadow-md rounded-xl p-6 mb-6 dark:bg-gray-800">
                <div class="flex items-center mb-4">
                    <div class="bg-yellow-500 dark:bg-green-500 rounded-full p-2">
                        <i class="fas fa-map-marker-alt text-white"></i>
                    </div>
                </div>
                <ul>
                    <li><strong>Country:</strong> Bangladesh</li>
                    <li><strong>City:</strong> Dhaka</li>
                    <li><strong>Street:</strong> 35 Vhatara, Badda</li>
                </ul>
            </div>
            <div class=" shadow-md rounded-xl p-6 mb-6 dark:bg-gray-800">
                <div class="flex items-center mb-4">
                    <div class="bg-yellow-500 dark:bg-green-500 rounded-full p-2">
                        <i class="fas fa-envelope text-white"></i>
                    </div>
                </div>
                <ul>
                    <li><strong>Email:</strong> Youremail@gmail.com</li>
                    <li><strong>Skype:</strong> @Yourusername</li>
                    <li><strong>Telegram:</strong> @Yourusername</li>
                </ul>
            </div>
            <div class=" shadow-md rounded-xl p-6 dark:bg-gray-800">
                <div class="flex items-center mb-4">
                    <div class="bg-yellow-500 dark:bg-green-500 rounded-full p-2">
                        <i class="fas fa-phone text-white"></i>
                    </div>
                </div>
                <ul>
                    <li><strong>Support Services:</strong> 15369</li>
                    <li><strong>Office:</strong> +58 (021)356 587 235</li>
                    <li><strong>Personal:</strong> +58 (021)356 587 235</li>
                </ul>
            </div>
        </div>

        <!-- Leave Us Your Info Form -->
        <div class="w-full md:w-1/2 p-4">
            <h2 class="text-3xl font-bold mb-4 dark:text-white">Leave Us Your Info</h2>
            <form class="shadow-md rounded-xl p-6 dark:bg-gray-800">
                <input type="text" placeholder="Your Full Name (Required)"
                    class="w-full mb-4 p-3 border rounded-md dark:text-black" />
                <input type="email" placeholder="Your Email (Required)"
                    class="w-full mb-4 p-3 border rounded-md dark:text-black" />
                <input type="text" placeholder="Subject" class="w-full mb-4 p-3 border rounded-md dark:text-black" />
                <textarea placeholder="Your Message"
                    class="w-full mb-4 p-3 border rounded-md dark:text-black"></textarea>
                <button class="bg-yellow-500 dark:bg-green-500 text-white px-6 py-2 rounded-md hover:bg-yellow-600">Send
                    Message</button>
            </form>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'Contact',
});
</script>

<style scoped>
h2 {
    color: #1a1a1a;
}
</style>
