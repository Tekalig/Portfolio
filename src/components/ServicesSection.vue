<template>
  <section class="py-16 text-center">
    <h2 class="text-4xl font-bold text-gray-900 dark:text-white">My Services</h2>
    <p class="text-gray-600 dark:text-gray-300 max-w-2xl mx-auto mt-4">
      Amet Minim Mollit Non Deserunt Ullamco Est Sit Aliqua Dolor.
      Do Amet Sint. Velit Officia Consequat Duis Enim Velit Mollit. Lorem Ipsum.
    </p>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 mt-12 max-w-5xl mx-auto">
      <div v-for="service in services" :key="service.title" class="flex flex-col items-center">
        <div class="text-yellow-500 text-5xl mb-4">
          <i :class="service.icon"></i>
        </div>
        <h3 class="text-xl font-semibold text-gray-900 dark:text-white">{{ service.title }}</h3>
        <p class="text-gray-600 dark:text-gray-400">{{ service.description }}</p>
      </div>
    </div>

    <button class="mt-8 px-6 py-3 bg-yellow-500 text-white font-bold rounded-lg shadow-md hover:bg-yellow-600">
      ORDER NOW →
    </button>
  </section>
</template>

<script>
export default {
  name: "ServicesSection",
  data() {
    return {
      services: [
        { title: "Web Development", description: "Blog, E-Commerce", icon: "fas fa-code" },
        { title: "UI/UX Design", description: "Mobile App, Website Design", icon: "fas fa-paint-brush" },
        { title: "Sound Design", description: "Voice Over, Beat Making", icon: "fas fa-microphone" },
        { title: "Game Design", description: "Character Design, Props & Objects", icon: "fas fa-gamepad" },
        { title: "Photography", description: "Portrait, Product Photography", icon: "fas fa-camera" },
        { title: "Advertising", description: "Marketing & Promotions", icon: "fas fa-bullhorn" },
      ],
    };
  },
};
</script>

<style scoped>
/* You can add extra styling here if needed */
</style>
