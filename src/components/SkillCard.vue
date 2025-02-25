<template>
    <div
        class="bg-gray-200 dark:bg-gray-800 text-gray-900 dark:text-white rounded-lg p-4 shadow-lg hover:shadow-xl transition duration-300">
        <h3 class="text-xl font-semibold mb-2 text-purple-600 dark:text-purple-400">{{ title }}</h3>
        <ul class="list-disc list-inside space-y-1">
            <li v-for="(item, index) in parsedItems" :key="index">{{ item }}</li>
        </ul>
    </div>
</template>

<script lang="ts">
import { computed, defineComponent } from 'vue';

export default defineComponent({
    name: 'SkillCard',
    props: {
        title: {
            type: String,
            required: true
        },
        skills: {
            type: String,
            default: ''
        }
    },
    setup(props) {
        const parsedItems = computed(() => props.skills.split(',').map(skill => skill.trim()));
        return { parsedItems };
    }
});
</script>
