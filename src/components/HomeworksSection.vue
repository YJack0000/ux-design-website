<template>
    <div>
        <div class="mx-auto max-w-screen-sm text-center mb-8 lg:mb-16">
            <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">
                Homeworks
            </h2>
        </div>
        <div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
            <HomeworkCard title="Contextual Inquiry" />
            <HomeworkCard title="Affinity Diagram" />
        </div>
    </div>
</template>
<script setup>
import HomeworkCard from '@/components/ui/HomeworkCard.vue'
</script>
