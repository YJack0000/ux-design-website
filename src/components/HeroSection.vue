<template>
    <section class="bg-white dark:bg-gray-900 overflow-hidden">
        <div
            class="grid min-h-[70vh] h-full max-w-screen-xl px-4 py-8 mx-auto lg:gap-8 xl:gap-0 lg:py-16 lg:grid-cols-12"
        >
            <div class="mr-auto place-self-center lg:col-span-7 z-10">
                <h1
                    class="max-w-2xl mb-4 text-4xl font-extrabold tracking-tight leading-none md:text-5xl xl:text-6xl dark:text-white"
                >
                    <div class="hidden-left">
                        <span class="text-4xl text-blue-500">2023,&nbsp;</span>
                        <span class="text-4xl">Semester 2</span>
                    </div>
                    <h1 class="hidden-left text-5xl font-bold">
                        <span class="text-blue-500">U</span>SER E<span class="text-blue-500">X</span
                        >PERIENCE
                    </h1>
                </h1>
                <p
                    class="hidden-left mt-4 max-w-2xl mb-6 font-light text-gray-500 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-400"
                >
                    This is the website of the course User Experience Design in NCCU. And we are the
                    <span class="text-blue-500">group 13</span> of this course.
                </p>
                <a
                    href="#"
                    class="inline-flex items-center justify-center px-5 py-3 mr-3 text-base font-medium text-center text-white rounded-lg bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:ring-primary-300 dark:focus:ring-primary-900"
                >
                    Get started
                    <svg
                        class="w-5 h-5 ml-2 -mr-1"
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
                </a>
            </div>
            <div
                class="hidden opacity-0 transition-all duration-[2s] lg:mt-0 lg:col-span-5 lg:flex overflow-visible"
            >
                <img class="h-fit my-auto scale-[1.3]" src="/mock.svg" alt="mockup" />
            </div>
        </div>
    </section>
</template>
<script setup>
import { onMounted } from 'vue'
onMounted(() => {
    const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
            if (entry.isIntersecting) {
                entry.target.classList.remove('opacity-0')
                entry.target.classList.add('opacity-100')
            } else {
                entry.target.classList.remove('opacity-100')
                entry.target.classList.add('opacity-0')
            }
        })
    })
    const observerLeft = new IntersectionObserver((entries) => {
        let count = 0
        entries.forEach((entry) => {
            setTimeout(() => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('show-left')
                } else {
                    entry.target.classList.remove('show-left')
                }
            }, count++ * 100)
        })
    })
    // const observerRight = new IntersectionObserver((entries) => {
    //     entries.forEach((entry) => {
    //         if (entry.isIntersecting) {
    //             entry.target.classList.add('show-right')
    //         } else {
    //             entry.target.classList.remove('show-right')
    //         }
    //     })
    // })

    let hiddenElements = []

    hiddenElements = document.querySelectorAll('.opacity-0')
    hiddenElements.forEach((element) => {
        observer.observe(element)
    })

    hiddenElements = document.querySelectorAll('.hidden-left')
    hiddenElements.forEach((element) => {
        observerLeft.observe(element)
    })

    // hiddenElements = document.querySelectorAll('.hidden-right')
    // hiddenElements.forEach((element) => {
    //     observerRight.observe(element)
    // })
})
</script>
