<template>
    <div
        class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
    >
        <a href="#">
            <img class="rounded-t-lg" src="" alt="" />
        </a>
        <div class="p-5 h-full">
            <div class="flex flex-col justify-between h-full">
                <div>
                    <a href="#">
                        <h5
                            class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                        >
                            {{ title }}
                        </h5>
                    </a>
                    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                        {{ description }}
                    </p>
                </div>
                <div>
                    <button
                        :data-modal-target="`${title}-modal`"
                        :data-modal-toggle="`${title}-modal`"
                        class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-500 rounded-lg hover:bg-blue-600 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-500 dark:hover:bg-blue-500 dark:focus:ring-blue-600"
                    >
                        Read more
                        <svg
                            aria-hidden="true"
                            class="w-4 h-4 ml-2 -mr-1"
                            fill="currentColor"
                            viewBox="0 0 20 20"
                            xmlns="http://www.w3.org/2000/svg"
                        >
                            <path
                                fill-rule="evenodd"
                                d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
                                clip-rule="evenodd"
                            ></path>
                        </svg>
                    </button>
                </div>
            </div>
            <HomeworkModal :title="title">
                <slot />
            </HomeworkModal>
        </div>
    </div>
</template>
<script setup>
import HomeworkModal from '@/components/homeworks/HomeworkModal.vue'

import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'

onMounted(() => {
    initFlowbite()
})

defineProps({
    title: {
        type: String,
        default: 'Project Title'
    },
    description: {
        type: String,
        default: 'Project Description'
    }
})
</script>
<style scoped>
section > * {
    margin-bottom: 1rem;
}

:deep(h1) {
    font-size: 2rem;
    font-weight: bold;
    margin-top: 2rem;
    margin-bottom: 1rem;
}
:deep(h2) {
    font-size: 1.5rem;
    font-weight: bold;
    margin-top: 1rem;
    margin-bottom: 0.5rem;
}
:deep(img) {
    width: 100%;
    max-width: 700px;
    height: auto;

    margin-left: auto;
    margin-right: auto;

    border-radius: 10px;
    transition: all 0.5s ease-in-out;
}
:deep(ul) {
    list-style-type: disc;
}
:deep(li) {
    margin-left: 2rem;
}
:deep(iframe) {
    width: 100%;
    height: 100%;
}
:deep(img:hover) {
    transform: scale(1.3);
}
</style>
