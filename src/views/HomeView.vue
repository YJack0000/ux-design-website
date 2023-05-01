<template>
    <header>
        <AppNavbar />
    </header>

    <HeroSection />
    <DefaultLayout>
        <MembersSection />
        <ProjectsSection />
    </DefaultLayout>
    <AppFooter />
</template>
<script setup>
import AppNavbar from '@/components/AppNavbar.vue'
import DefaultLayout from '@/layouts/DefaultLayout.vue'
import HeroSection from '@/components/HeroSection.vue'
import MembersSection from '@/components/MembersSection.vue'
import ProjectsSection from '@/components/ProjectsSection.vue'
import AppFooter from '@/components/AppFooter.vue'
</script>
<style scoped></style>
