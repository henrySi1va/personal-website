<script setup>
import Experience from '@/components/Experience.vue'

import experienceData from '@/experiences.json';
import { ref } from 'vue';

const experiences = ref(experienceData);
</script>

<template>
<section class="max-w-6xl mx-auto py-8 space-y-12">
    <h2 class="text-3xl font-semibold text-white mb-6">Work Experience</h2>
    <Experience v-for="experience in experiences" :key="experience.title" :experience="experience" />
</section>
</template>