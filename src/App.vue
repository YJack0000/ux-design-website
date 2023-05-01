<template>
    <RouterView />
</template>
<script setup>
import { RouterView } from 'vue-router'

import { onMounted } from 'vue'
import { 
    initAccordions, 
    initCarousels, 
    initCollapses, 
    initDials, 
    initDismisses, 
    initDrawers, 
    initDropdowns, 
    initModals, 
    initPopovers, 
    initTabs, 
    initTooltips } from 'flowbite'

// initialize components based on data attribute selectors
onMounted(() => {
    initAccordions();
    initCarousels();
    initCollapses();
    initDials();
    initDismisses();
    initDrawers();
    initDropdowns();
    initModals();
    initPopovers();
    initTabs();
    initTooltips();
})
</script>
<style>
.hidden-1 {
    opacity: 0;
    transition: all 1s ease-in-out;
}
@media(prefers-reduced-motion) {
    .hidden-1 {
        transition: none;
    }
}
.show-1 {
    opacity: 1;
}
.hidden-left {
    opacity: 0;
    transition: all 2s;
    transform: translateX(-300px);
}
@media(prefers-reduced-motion) {
    .hidden-left {
        transition: none;
    }
}
.show-left {
    opacity: 1;
    transform: translateX(0);
}
.hidden-right {
    opacity: 0;
    transition: all 2s;
    transform: translateX(300px);
}
@media(prefers-reduced-motion) {
    .hidden-right {
        transition: none;
    }
}
.show-right {
    opacity: 1;
    transform: translateX(0);
}
</style>
