<template>
    <div class=" sticky top-0 right-0 h-full overflow-y-auto">
        <div class="w-96 bg-gray-100 shadow-lg rounded-lg p-6 dark:bg-gray-800">
            <div class="flex flex-col items-center">
                <img class="w-24 h-24 rounded-full border-4 border-gray-300" src="https://via.placeholder.com/100" alt="Profile" />
                <h2 class="mt-4 text-lg font-semibold">Tekalign Mesfin</h2>
                <p class="text-gray-500">Full-Stack Developer and Data Scientests</p>
            </div>
            <div class="flex justify-center space-x-3 mt-4">
                <font-awesome-icon :icon="['fab', 'facebook']" class="text-yellow-500"></font-awesome-icon>
                <font-awesome-icon :icon="['fab', 'instagram']" class="text-yellow-500"></font-awesome-icon>
                <font-awesome-icon :icon="['fab', 'twitter']" class="text-yellow-500"></font-awesome-icon>
                <font-awesome-icon :icon="['fab', 'linkedin']" class="text-yellow-500"></font-awesome-icon>
                <font-awesome-icon :icon="['fab', 'dribbble']" class="text-yellow-500"></font-awesome-icon>
            </div>
            <div class="mt-6">
                <p><span class="font-bold text-yellow-500">Age:</span> 23</p>
                <p><span class="font-bold text-yellow-500">Residence:</span> ET</p>
                <p><span class="font-bold text-yellow-500">Freelance:</span> <span class="text-green-500">Available</span></p>
                <p><span class="font-bold text-yellow-500">Address:</span> Addis Ababa, Arada</p>
            </div>
            <div class="mt-6">
                <h3 class="font-semibold">Languages</h3>
                <div v-for="lang in languages" :key="lang.name" class="mt-2">
                    <p>{{ lang.name }} {{ lang.percentage }}%</p>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-yellow-500 h-2.5 rounded-full" :style="{ width: lang.percentage + '%' }"></div>
                    </div>
                </div>
            </div>
            <div class="mt-6">
                <h3 class="font-semibold">Skills</h3>
                <div v-for="skill in skills" :key="skill.name" class="mt-2">
                    <p>{{ skill.name }} {{ skill.percentage }}%</p>
                    <div class="w-full bg-gray-200 rounded-full h-2.5">
                        <div class="bg-yellow-500 h-2.5 rounded-full" :style="{ width: skill.percentage + '%' }"></div>
                    </div>
                </div>
            </div>
            <div class="mt-6">
                <h3 class="font-semibold">Extra Skills</h3>
                <ul class="list-disc ml-5">
                    <li>Bootstrap, Materialize</li>
                    <li>Stylus, Tailwind, Less</li>
                    <li>Gulp, Webpack, Grunt</li>
                    <li>GIT Knowledge</li>
                </ul>
            </div>
            <div class="mt-6 text-center">
                <button class="bg-yellow-500 text-white px-4 py-2 rounded-lg">Download CV</button>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { library } from '@fortawesome/fontawesome-svg-core';
import { faFacebook, faInstagram, faTwitter, faLinkedin, faDribbble } from '@fortawesome/free-brands-svg-icons';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { defineComponent } from 'vue';

library.add(faFacebook, faInstagram, faTwitter, faLinkedin, faDribbble);

export default defineComponent({
    name: 'ProfileCard',
    components: {
        FontAwesomeIcon
    },
    data() {
        return {
            languages: [
                { name: "Amaric", percentage: 100 },
                { name: "English", percentage: 80 },
                { name: "Oromia", percentage: 60 },
            ],
            skills: [
                { name: "Html", percentage: 90 },
                { name: "CSS", percentage: 85 },
                { name: "Js", percentage: 90 },
                { name: "Python", percentage: 85 },
                { name: "Figma", percentage: 65 },
            ],
        };
    },
});
</script>

<style>
@import "animate.css/animate.min.css";
</style>
