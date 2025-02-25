<template>
  <section class="min-h-screen bg-gray-50 dark:bg-gray-900 text-gray-900 dark:text-white py-12 px-6">
    <div class="container mx-auto max-w-5xl">
      <h1 class="text-4xl font-bold text-purple-500 dark:text-purple-400 mb-4">/about-me</h1>
      <p class="text-lg mb-12">Who am I?</p>

      <div class="mb-12">
        <h2 class="text-2xl font-bold mb-4">Hello, I’m Tekalign!</h2>
        <p class="mb-4">
          I’m a self-taught front-end developer based in Kyiv, Ukraine. I can develop responsive websites from scratch and raise them into modern user-friendly web experiences.
        </p>
        <p>
          Transforming my creativity and knowledge into a websites has been my passion for over a year. I have been helping various clients to establish their presence online. I always strive to learn about the newest technologies and frameworks.
        </p>
      </div>

      <h2 class="text-3xl text-purple-500 dark:text-purple-400 font-bold mb-6">#skills</h2>
      <div class="grid gap-4 lg:grid-cols-3 md:grid-cols-2">
        <SkillCard title="Languages" skills="TypeScript, Go, C, C++, Python, JavaScript" />
        <SkillCard title="Other" skills="HTML, CSS, EJS, Docker, REST, Jinja" />
        <SkillCard title="Tools" skills="VSCode, Linux, Figma, Git, Font Awesome, KDE" />
        <SkillCard title="Databases" skills="MySql, PostgreSQL, Mongo" />
        <SkillCard title="Frameworks" skills="React, Vue, Deno, Flask, Express.js" />
      </div>

      <h2 class="text-3xl text-purple-500 dark:text-purple-400 font-bold mt-12 mb-6">#my-fun-facts</h2>
      <div class="flex flex-wrap gap-4">
        <span class="dark:bg-gray-800 bg-gray-100 py-2 px-4 rounded">I like winter more than summer</span>
        <span class="dark:bg-gray-800 bg-gray-100 py-2 px-4 rounded">I often bike with my friends</span>
        <span class="dark:bg-gray-800 bg-gray-100 py-2 px-4 rounded">I like pizza and pasta</span>
        <span class="dark:bg-gray-800 bg-gray-100 py-2 px-4 rounded">I was in Egypt, Poland and Turkey</span>
        <span class="dark:bg-gray-800 bg-gray-100 py-2 px-4 rounded">My favorite movie is The Green Mile</span>
        <span class="dark:bg-gray-800 bg-gray-100 py-2 px-4 rounded">I am still in school</span>
        <span class="dark:bg-gray-800 bg-gray-100 py-2 px-4 rounded">I don’t have any siblings</span>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import SkillCard from '../components/SkillCard.vue';
import { defineComponent } from 'vue';

export default defineComponent({
  components: {
    SkillCard,
  },
});
</script>

<style scoped>
body {
  transition: background-color 0.3s ease;
}
</style>
