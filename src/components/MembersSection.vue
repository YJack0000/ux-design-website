<template>
    <section class="bg-white dark:bg-gray-900">
        <div class="py-8 px-4 mx-auto max-w-screen-xl lg:py-16 lg:px-6">
            <div class="mx-auto max-w-screen-sm text-center mb-8 lg:mb-16">
                <h2
                    class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white"
                >
                    Our Team
                </h2>
                <p class="font-light text-gray-500 lg:mb-16 sm:text-xl dark:text-gray-400">
                    We are a team of students from different majors in NCCU. We are passionate about
                    the topic of the project and hope to learn more about it.
                </p>
            </div>
            <div class="grid gap-8 mb-6 lg:mb-16 md:grid-cols-2">
                <MemberCard
                    class="mc hidden-1"
                    image="/morgan.png"
                    name="Ting-Yi, Lin"
                    department="Department of Advertising"
                    description="Ting-Yi is a designer in Advertising and a freelancer."
                />
                <MemberCard
                    class="mc hidden-1"
                    image="/tymek.png"
                    name="Tymek Jagielski"
                    department="Exchange Student from Poland"
                    description="Tymek is a student from poland and major in diplomacy."
                />
                <MemberCard
                    class="mc hidden-1"
                    image="/ashlee.png"
                    name="Yun-Hsin, Tsai"
                    department="Department of BA"
                    description="Yun-Hsin is a good student."
                />
                <MemberCard
                    class="mc hidden-1"
                    image="/yu-jie.jpg"
                    name="Yu-Jie, Zheng"
                    department="Department of CS"
                    description="Yu-Jie is a frontend developer and active in Vue.js community."
                />
            </div>
        </div>
    </section>
</template>
<script setup>
import { onMounted } from 'vue'
import MemberCard from '@/components/ui/MemberCard.vue'

onMounted(() => {
    let count = 0
    const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
            setTimeout(() => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('show-1')
                } else {
                    entry.target.classList.remove('show-1')
                }
            }, count * 400)

            if (entry.isIntersecting) count += 1
            if (count > 3) count = 0
        })
    })

    const elements = document.querySelectorAll('.mc.hidden-1')

    elements.forEach((element) => {
        observer.observe(element)
    })
})
</script>
