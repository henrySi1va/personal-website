<template>
<body class="p-4 sm:p-8">

  <!-- Hero Section -->
  <section class="flex flex-col md:flex-row items-center md:items-start gap-8 max-w-6xl mx-auto py-12">
    <!-- Photo -->
    <img src="./assets/me.jpg" alt="Your photo" class="w-48 h-48 rounded-full object-cover shadow-lg" />

    <!-- Name and Bio -->
    <div class="flex-1">
      <h1 class="text-4xl sm:text-5xl font-bold text-white mb-4">Henry Silva</h1>
      <p class="text-lg mb-6 max-w-xl">
        Just a guy.
      </p>

      <!-- Social Links -->
      <div class="flex gap-4">
        <a href="https://github.com/henrySi1va" target="_blank" class="hover:text-white">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 .5C5.65.5.5 5.65.5 12c0 5.1 3.3 9.4 7.9 10.9.6.1.8-.3.8-.6v-2.1c-3.2.7-3.9-1.5-3.9-1.5-.6-1.5-1.4-1.9-1.4-1.9-1.1-.8.1-.8.1-.8 1.2.1 1.8 1.3 1.8 1.3 1.1 1.9 2.9 1.4 3.6 1.1.1-.8.4-1.4.7-1.7-2.6-.3-5.3-1.3-5.3-5.9 0-1.3.5-2.3 1.2-3.2-.1-.3-.5-1.5.1-3.2 0 0 1-.3 3.3 1.2a11.4 11.4 0 0 1 6 0c2.3-1.5 3.3-1.2 3.3-1.2.6 1.7.2 2.9.1 3.2.8.9 1.2 2 1.2 3.2 0 4.7-2.7 5.6-5.3 5.9.4.3.8 1 .8 2v3c0 .3.2.7.8.6A10.9 10.9 0 0 0 23.5 12c0-6.35-5.15-11.5-11.5-11.5z"/>
          </svg>
        </a>
        <a href="https://www.linkedin.com/in/henry2000/" target="_blank" class="hover:text-white">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
            <path d="M4.98 3.5C4.98 4.88 3.87 6 2.5 6S0 4.88 0 3.5 1.12 1 2.5 1s2.48 1.12 2.48 2.5zM.5 8h4v12h-4zM7.5 8h3.7v1.6h.1c.5-.9 1.6-1.8 3.3-1.8 3.5 0 4.2 2.3 4.2 5.3V20h-4v-5.3c0-1.3 0-3-1.8-3-1.8 0-2 1.4-2 2.9V20h-4z"/>
          </svg>
        </a>
      </div>
    </div>
  </section>

  <!-- Projects Section -->
  <section class="max-w-6xl mx-auto py-8 space-y-12">
    <h2 class="text-3xl font-semibold text-white mb-6">Things I've Worked On</h2>

    <!-- Project 1 -->
    <div class="flex flex-col md:flex-row items-center gap-6">
      <img src="https://via.placeholder.com/300x200" alt="Project 1" class="w-full md:w-64 rounded-lg shadow-md" />
      <div>
        <h3 class="text-2xl font-bold text-white mb-2">Smart Scheduler</h3>
        <p>A web app that automatically schedules meetings across multiple calendars using AI. Built with Node.js, React, and Tailwind CSS.</p>
      </div>
    </div>

    <!-- Project 2 -->
    <div class="flex flex-col md:flex-row items-center gap-6">
      <img src="https://via.placeholder.com/300x200" alt="Project 2" class="w-full md:w-64 rounded-lg shadow-md" />
      <div>
        <h3 class="text-2xl font-bold text-white mb-2">Portfolio Tracker</h3>
        <p>An investment portfolio tracker for crypto and stocks with real-time charts and analytics. Built with Vue.js and Firebase.</p>
      </div>
    </div>

    <!-- Project 3 -->
    <div class="flex flex-col md:flex-row items-center gap-6">
      <img src="https://via.placeholder.com/300x200" alt="Project 3" class="w-full md:w-64 rounded-lg shadow-md" />
      <div>
        <h3 class="text-2xl font-bold text-white mb-2">DevBlog Platform</h3>
        <p>A Markdown-based blogging platform tailored for developers. Supports code snippets, LaTeX, and dark mode. Built with Next.js.</p>
      </div>
    </div>

  </section>
</body>

</template>
