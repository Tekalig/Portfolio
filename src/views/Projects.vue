<template>
    <section class="dark:bg-gray-900 dark:text-white min-h-screen py-12 px-6 max-w-5xl">
        <div class="container mx-auto">
            <h1 class="text-5xl font-bold mb-4 text-gray-100">/projects</h1>
            <p class="text-lg text-gray-400 mb-12">List of my projects</p>

            <h2 class="text-3xl text-purple-500 font-bold mb-6">#complete-apps</h2>
            <div class="grid gap-8 lg:grid-cols-3 md:grid-cols-2">
                <ProjectCard title="ChertNodes" description="Minecraft servers hosting" tech="HTML SCSS Python Flask"
                    liveLink="#" cachedLink="#" image="https://via.placeholder.com/300x200" />
                <ProjectCard title="Kahoot Answers Viewer" description="Get answers to your kahoot quiz"
                    tech="CSS Express Node.js" liveLink="#" image="https://via.placeholder.com/300x200" />
                <ProjectCard title="ProtectX" description="Discord anti-crash bot"
                    tech="React Express Discord.js Node.js" cachedLink="#"
                    image="https://via.placeholder.com/300x200" />
                <ProjectCard title="Kotik Bot" description="Multi-functional discord bot" tech="HTML CSS JS"
                    liveLink="#" image="https://via.placeholder.com/300x200" />
                <ProjectCard title="Portfolio" description="You’re using it rn" tech="Vue TS Less" githubLink="#"
                    image="https://via.placeholder.com/300x200" />
            </div>

            <h2 class="text-3xl text-purple-500 font-bold mt-16 mb-6">#small-projects</h2>
            <div class="grid gap-8 lg:grid-cols-3 md:grid-cols-2">
                <ProjectCard title="Bot boilerplate"
                    description="Start creating scalable discord.js bot with typescript" tech="Discord.js TS JS"
                    githubLink="#" image="https://via.placeholder.com/300x200" />
                <ProjectCard title="My blog" description="Front-end of my future blog website written in Vue"
                    tech="VUE CSS JS" githubLink="#" image="https://via.placeholder.com/300x200" />
                <ProjectCard title="Chess pro" description="Landing page for chess tournaments" tech="Figma"
                    figmaLink="#" image="https://via.placeholder.com/300x200" />
                <ProjectCard title="Crash protect website" description="Anti-raid, anti-crash discord bot template"
                    tech="Figma" figmaLink="#" image="https://via.placeholder.com/300x200" />
                <ProjectCard title="CSS experiments" description="Collection of my little projects in CSS"
                    tech="HTML CSS" liveLink="#" image="https://via.placeholder.com/300x200" />
            </div>
        </div>
    </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ProjectCard from "../components/ProjectCard.vue";

export default defineComponent({
    name: 'Projects',
    components: {ProjectCard}
});
</script>
