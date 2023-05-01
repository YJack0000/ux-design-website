<template>
    <header>
        <AppNavbar />
    </header>

    <HeroSection id="hero" />
    <DefaultLayout>
        <MembersSection id="members" />
        <HomeworksSection id="homeworks" />
    </DefaultLayout>
    <AppFooter />
</template>
<script setup>
import AppNavbar from '@/components/AppNavbar.vue'
import DefaultLayout from '@/layouts/DefaultLayout.vue'
import HeroSection from '@/components/HeroSection.vue'
import MembersSection from '@/components/MembersSection.vue'
import HomeworksSection from '@/components/HomeworksSection.vue'
import AppFooter from '@/components/AppFooter.vue'
</script>
<style scoped></style>
