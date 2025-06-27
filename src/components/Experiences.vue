<script setup>
import Experience from '@/components/Experience.vue'

const experiences = [
  {
    title: 'Co-Founder & Director of Product Development',
    company: 'Wavelogix',
    duration: 'January 2023 - May 2025',
    description: ['Lead multi-disciplinary engineering and research team to completely overhaul our innovative concrete sensor product to be market ready in 18 months.',
                  'Built product team from the ground up spanning embedded firmware, hardware design, machine learning, and full-stack development.',
                  'Aligned product development milestones to company GTM strategy by deploying an MVP in 8 states across the US in the summer of 2023.',
                  'Transformed management strategy by removing silos to make each member independent and cross-functional which reduced management overhead.'],
    links: [
      'https://wavelogix.tech',
      'https://www.linkedin.com/company/wavelogix-inc']
  }]
</script>

<template>
<section class="max-w-6xl mx-auto py-8 space-y-12">
    <h2 class="text-3xl font-semibold text-white mb-6">Work Experience</h2>
    <Experience v-for="experience in experiences" :key="experience.title" :experience="experience" />
</section>
</template>