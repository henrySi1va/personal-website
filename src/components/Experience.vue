<script setup>
defineProps(
    {
        experience: {
        type: Object,
        },
    }
)
</script>

<template>
<div class="flex flex-col md:flex-row items-center gap-6">
    <div>
      <div class="flex items-baseline gap-3">
        <h3 class="text-2xl font-bold text-white mb-1">{{ experience.title }}</h3>
      </div>
      <div class="text-md text-gray-400 mb-2">{{ experience.company }}, {{ experience.duration }}</div>
      <ul class="list-disc list-inside text-white mt-2">
        <li v-for="(item, index) in experience.description" :key="index">{{ item }}</li>
      </ul>
      <div v-if="experience.links && experience.links.length" class="flex gap-3 mt-2">
        <a
          v-for="(link, idx) in experience.links"
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
          <span v-else-if="link.includes('linkedin.com')" aria-label="LinkedIn">
            <!-- LinkedIn SVG Icon -->
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 inline" fill="currentColor" viewBox="0 0 24 24">
              <path d="M4.98 3.5C4.98 4.88 3.87 6 2.5 6S0 4.88 0 3.5 1.12 1 2.5 1s2.48 1.12 2.48 2.5zM.5 8h4v12h-4zM7.5 8h3.7v1.6h.1c.5-.9 1.6-1.8 3.3-1.8 3.5 0 4.2 2.3 4.2 5.3V20h-4v-5.3c0-1.3 0-3-1.8-3-1.8 0-2 1.4-2 2.9V20h-4z"/>
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
</div>
</template>