<template>
    <section class="bg-white dark:text-white dark:bg-gray-800 py-16">
        <div class="container mx-auto px-4 max-w-4xl">
            <div class="text-center mb-8">
                <h2 class="text-4xl font-bold">Education</h2>
                <p class="text-gray-400 mt-2">
                    Amet Minim Mollit Non Deserunt Ullamco Est Sit Aliqua Dolor<br />
                    Do Amet Sint, Velit Officia Consequat Duis Enim Velit Mollit.<br />
                    Lorem Ipsum
                </p>
            </div>

            <div class="bg-white text-black dark:bg-gray-800 dark:text-white rounded-lg shadow-md p-8 space-y-8">
                <div class="flex flex-col space-y-8">
                    <div v-for="(item, index) in educationList" :key="index" class="border-b pb-4">
                        <div class="flex justify-between items-start">
                            <div>
                                <h3 class="text-xl font-semibold">{{ item.institution }}</h3>
                                <p class="text-gray-500">{{ item.role }}</p>
                            </div>
                            <span class="bg-yellow-400 dark:bg-green-500 text-black px-3 py-1 rounded-full">
                                {{ item.date }}
                            </span>
                        </div>
                        <h4 class="text-lg font-medium mt-2">{{ item.certificate }}</h4>
                        <p class="text-gray-600">{{ item.description }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script lang="ts">
import { defineComponent, reactive } from 'vue'

export default defineComponent({
    name: 'Education',
    setup() {
        const educationList = reactive([
            {
                institution: "University Of Toronto",
                role: "Student",
                date: "Jan 1016 - Dec 2021",
                certificate: "Certificate Of Web Training",
                description: "Lorem Ipsum Dolor Sit Amet, Consectetur Adipiscing Elit. Amet Dapibus Nibh Ut Faucibus Nunc, Egestas Id Amet Porttitor. Pulvinar Quisque Sed Amet, Nulla Nunc. Eleifend Sodales Posuere Fusce Tempus Etiam Et Pellentesque. Molestie Risus Enim Neque Eget Dui."
            },
            {
                institution: "Programming Course",
                role: "Student",
                date: "Jan 1016 - Dec 2021",
                certificate: "Certificate Of Web Training",
                description: "Lorem Ipsum Dolor Sit Amet, Consectetur Adipiscing Elit. Amet Dapibus Nibh Ut Faucibus Nunc, Egestas Id Amet Porttitor. Pulvinar Quisque Sed Amet, Nulla Nunc. Eleifend Sodales Posuere Fusce Tempus Etiam Et Pellentesque. Molestie Risus Enim Neque Eget Dui."
            },
            {
                institution: "Web Developer Courses",
                role: "Student",
                date: "Jan 1016 - Dec 2021",
                certificate: "Certificate Of Web Training",
                description: "Lorem Ipsum Dolor Sit Amet, Consectetur Adipiscing Elit. Amet Dapibus Nibh Ut Faucibus Nunc, Egestas Id Amet Porttitor. Pulvinar Quisque Sed Amet, Nulla Nunc. Eleifend Sodales Posuere Fusce Tempus Etiam Et Pellentesque. Molestie Risus Enim Neque Eget Dui."
            }
        ])

        return {
            educationList
        }
    }
})
</script>
