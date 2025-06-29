<script setup>
import Project from '@/components/Project.vue';

import projectData from '@/projects.json';
import { ref } from 'vue';

const projects = ref(projectData);
</script>

<template>
<section class="max-w-6xl mx-auto py-8 space-y-12">
    <h2 class="text-3xl font-semibold text-white mb-6">Personal Projects</h2>
    <Project v-for="project in projects" :key="project.title" :project="project" />
</section>
</template>