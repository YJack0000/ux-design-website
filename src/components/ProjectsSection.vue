<template>
    <div>
        <div class="mx-auto max-w-screen-sm text-center mb-8 lg:mb-16">
            <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">
                Homeworks
            </h2>
        </div>
        <div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
            <ProjectCard title="Contextual Inquiry" />
            <ProjectCard title="Affinity Diagram" />
        </div>
    </div>
</template>
<script setup>
import ProjectCard from '@/components/ProjectCard.vue'
</script>
