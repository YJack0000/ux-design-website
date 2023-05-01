<template>
    <div
        class="items-center bg-gray-50 rounded-lg shadow flex dark:bg-gray-800 dark:border-gray-700"
    >
        <div>
            <img
                class="max-w-[200px] rounded-lg sm:rounded-none sm:rounded-l-lg"
                :src="imageUrl"
                alt="morgan Avatar"
            />
        </div>
        <div class="p-5 md:w-[35vw]">
            <h3 class="text-xl font-bold tracking-tight text-gray-900 dark:text-white">
                <div>{{ name }}</div>
            </h3>
            <span class="text-gray-500 dark:text-gray-400">{{ department }}</span>
            <p class="mt-3 mb-4 font-light text-gray-500 dark:text-gray-400">
                {{ description }}
            </p>
        </div>
    </div>
</template>
<script setup>
import { computed } from 'vue'
const props = defineProps(['image', 'name', 'department', 'description'])

const imageUrl = computed(() => {
    if(import.meta.env.PROD)
        return `/ux-design-website${props.image}`
    else 
        return props.image
})
</script>