<template>
    <section class="py-16 dark:bg-gray-900">
        <div class="text-center mb-8">
            <h2 class="text-4xl font-bold">Work History</h2>
            <p class="text-gray-400 mt-2">
                Amet Minim Mollit Non Deserunt Ullamco Est Sit Aliqua Dolor<br />
                Do Amet Sint, Velit Officia Consequat Duis Enim Velit Mollit.<br />
                Lorem Ipsum
            </p>
        </div>

        <div class="bg-white text-black rounded-lg shadow-md p-8 space-y-8 max-w-5xl mx-auto dark:bg-gray-800 dark:text-white">
            <div class="flex flex-col space-y-8">
                <div v-for="(item, index) in workHistory" :key="index" class="border-b pb-4">
                    <div class="flex justify-between items-start">
                        <div>
                            <h3 class="text-xl font-semibold">{{ item.position }}</h3>
                            <p class="text-gray-500">{{ item.role }}</p>
                        </div>
                        <span class="bg-yellow-400 text-black px-3 py-1 rounded-full">
                            {{ item.date }}
                        </span>
                    </div>
                    <h4 class="text-lg font-medium mt-2">{{ item.certificate }}</h4>
                    <p class="text-gray-600">{{ item.description }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script lang="ts">
import { reactive, defineComponent } from 'vue'

export default defineComponent( {
    name: 'WorkHistory',
    setup() {
        const workHistory = reactive([
            {
                position: "Lead Web Designer",
                role: "Student",
                date: "Jan 2016 - Dec 2021",
                certificate: "Certificate Of Web Training",
                description: "Lorem Ipsum Dolor Sit Amet, Consectetur Adipiscing Elit. Amet Dapibus Nibh Ut Faucibus Nunc, Egestas Id Amet Porttitor. Pulvinar Quisque Sed Amet, Nulla Nunc. Eleifend Sodales Posuere Fusce Tempus Etiam Et Pellentesque. Molestie Risus Enim Neque Eget Dui."
            },
            {
                position: "Junior Web Designer",
                role: "Student",
                date: "Jan 1016 - Dec 2021",
                certificate: "Certificate Of Web Training",
                description: "Lorem Ipsum Dolor Sit Amet, Consectetur Adipiscing Elit. Amet Dapibus Nibh Ut Faucibus Nunc, Egestas Id Amet Porttitor. Pulvinar Quisque Sed Amet, Nulla Nunc. Eleifend Sodales Posuere Fusce Tempus Etiam Et Pellentesque. Molestie Risus Enim Neque Eget Dui."
            },
            {
                position: "Senior Web Designer",
                role: "Student",
                date: "Jan 1016 - Dec 2021",
                certificate: "Certificate Of Web Training",
                description: "Lorem Ipsum Dolor Sit Amet, Consectetur Adipiscing Elit. Amet Dapibus Nibh Ut Faucibus Nunc, Egestas Id Amet Porttitor. Pulvinar Quisque Sed Amet, Nulla Nunc. Eleifend Sodales Posuere Fusce Tempus Etiam Et Pellentesque. Molestie Risus Enim Neque Eget Dui."
            }
        ])

        return {
            workHistory
        }
    }
})
</script>
