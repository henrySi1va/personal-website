<script setup>
defineProps(
    {
        project: {
        type: Object,
        },
    }
)
</script>

<template>
<div class="flex flex-col md:flex-row items-center gap-6">
    <div>
    <h3 class="text-2xl font-bold text-white mb-2">{{ project.title }}</h3>
    <p>{{ project.description }}</p>
    <div v-if="project.links && project.links.length" class="flex gap-3 mt-2">
      <a
        v-for="(link, idx) in project.links"
        :key="idx"
        :href="link"
        target="_blank"
        rel="noopener noreferrer"
        class="text-white hover:text-gray-400"
      >
        <span v-if="link.includes('github.com')" aria-label="GitHub">
          <!-- GitHub SVG Icon -->
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 inline" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 .5C5.73.5.5 5.73.5 12c0 5.08 3.29 9.39 7.86 10.91.58.11.79-.25.79-.56 0-.28-.01-1.02-.02-2-3.2.7-3.88-1.54-3.88-1.54-.53-1.34-1.3-1.7-1.3-1.7-1.06-.73.08-.72.08-.72 1.17.08 1.79 1.2 1.79 1.2 1.04 1.78 2.73 1.27 3.4.97.11-.75.41-1.27.74-1.56-2.56-.29-5.26-1.28-5.26-5.7 0-1.26.45-2.29 1.19-3.1-.12-.29-.52-1.46.11-3.04 0 0 .97-.31 3.18 1.18a11.1 11.1 0 0 1 2.9-.39c.99 0 1.99.13 2.9.39 2.2-1.49 3.17-1.18 3.17-1.18.63 1.58.23 2.75.11 3.04.74.81 1.19 1.84 1.19 3.1 0 4.43-2.7 5.41-5.27 5.7.42.36.79 1.08.79 2.18 0 1.57-.01 2.84-.01 3.23 0 .31.21.68.8.56C20.71 21.39 24 17.08 24 12c0-6.27-5.23-11.5-12-11.5z"/>
          </svg>
        </span>
        <span v-else aria-label="External Link">
          <!-- General Link SVG Icon -->
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 inline" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13.828 10.172a4 4 0 010 5.656l-3.535 3.535a4 4 0 01-5.657-5.657l1.414-1.414M10.172 13.828a4 4 0 010-5.656l3.535-3.535a4 4 0 015.657 5.657l-1.414 1.414"/>
          </svg>
        </span>
      </a>
    </div>
    </div>
    <img :src="project.imageUrl" :alt="project.title" class="w-full md:w-64 rounded-lg shadow-md" />
</div>
</template>