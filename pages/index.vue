<template>
  <div class="min-h-screen bg-white dark:bg-gray-900">
    <Navbar />
    
    <!-- Hero Section -->
    <section id="home" class="pt-32 pb-20 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto text-center">
        <h1 class="text-5xl md:text-6xl font-bold text-gray-900 dark:text-white mb-6">
          Hi, I'm <span class="text-blue-600 dark:text-blue-400">Dick Roldan Alambra</span>
        </h1>
        <p class="text-xl md:text-2xl text-gray-600 dark:text-gray-300 mb-8 max-w-3xl mx-auto">
          An Information Technology professional specializing in practical, innovative solutions. 
          I bridge technology and business needs by building modern web applications that solve real-world problems.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a
            href="#projects"
            class="inline-flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700 transition-colors"
          >
            View My Work
            <svg class="ml-2 h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </a>
          <a
            href="#contact"
            class="inline-flex items-center justify-center px-8 py-3 border border-gray-300 dark:border-gray-600 text-base font-medium rounded-md text-gray-700 dark:text-gray-300 bg-white dark:bg-gray-800 hover:bg-gray-50 dark:hover:bg-gray-700 transition-colors"
          >
            Contact Me
          </a>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50 dark:bg-gray-800">
      <div class="max-w-7xl mx-auto">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-4">About Me</h2>
          <p class="text-lg text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            As an Information Technology professional, I focus on practical technology solutions that drive business value. 
            I specialize in developing and implementing systems that are not just technically sound, but also user-friendly and aligned with organizational goals.
          </p>
        </div>
        
        <div class="grid md:grid-cols-2 gap-8">
          <!-- Background Card -->
          <div class="bg-white dark:bg-gray-900 rounded-lg shadow-md p-8">
            <div class="flex items-center mb-4">
              <svg class="h-8 w-8 text-blue-600 dark:text-blue-400 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
              </svg>
              <h3 class="text-2xl font-semibold text-gray-900 dark:text-white">Background</h3>
            </div>
            <p class="text-gray-600 dark:text-gray-300">
              With a degree in Information Technology and hands-on experience in system implementation, 
              I bring a practical, solutions-focused approach to development. My IT background enables me to 
              understand both the technical and business aspects of every project, ensuring solutions that truly work.
            </p>
          </div>
          
          <!-- Approach Card -->
          <div class="bg-white dark:bg-gray-900 rounded-lg shadow-md p-8">
            <div class="flex items-center mb-4">
              <svg class="h-8 w-8 text-blue-600 dark:text-blue-400 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              <h3 class="text-2xl font-semibold text-gray-900 dark:text-white">Approach</h3>
            </div>
            <p class="text-gray-600 dark:text-gray-300">
              I apply IT best practices to deliver reliable, maintainable solutions. 
              My approach combines technical expertise with business acumen—focusing on user needs, 
              system efficiency, and long-term sustainability to create technology that makes a real impact.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-4">Skills & Expertise</h2>
          <p class="text-lg text-gray-600 dark:text-gray-300">
            A comprehensive set of technical skills and tools I use to bring ideas to life.
          </p>
        </div>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div
            v-for="skill in skills"
            :key="skill.title"
            class="bg-white dark:bg-gray-800 rounded-lg shadow-md p-6 hover:shadow-lg transition-shadow"
          >
            <div class="text-blue-600 dark:text-blue-400 mb-4">
              <component :is="skill.icon" class="h-12 w-12" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">{{ skill.title }}</h3>
            <p class="text-gray-600 dark:text-gray-300">{{ skill.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50 dark:bg-gray-800">
      <div class="max-w-7xl mx-auto">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-4">Featured Projects</h2>
          <p class="text-lg text-gray-600 dark:text-gray-300">
            Here are some of my recent projects that showcase my skills and experience.
          </p>
        </div>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div
            v-for="project in projects"
            :key="project.title"
            class="bg-white dark:bg-gray-900 rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow"
          >
            <img
              :src="project.image"
              :alt="project.title"
              class="w-full h-48 object-cover"
              @error="handleImageError"
            />
            <div class="p-6">
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">{{ project.title }}</h3>
              <p class="text-gray-600 dark:text-gray-300 mb-4">{{ project.description }}</p>
              <div class="flex flex-wrap gap-2 mb-4">
                <span
                  v-for="tag in project.tags"
                  :key="tag"
                  class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200 text-sm rounded-full"
                >
                  {{ tag }}
                </span>
              </div>
              <a
                :href="project.link"
                class="inline-flex items-center text-blue-600 dark:text-blue-400 hover:text-blue-700 dark:hover:text-blue-300 font-medium"
              >
                View Project
                <svg class="ml-2 h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
                </svg>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 px-4 sm:px-6 lg:px-8">
      <div class="max-w-4xl mx-auto text-center">
        <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-4">Let's Work Together</h2>
        <p class="text-lg text-gray-600 dark:text-gray-300 mb-8">
          Interested in collaborating or have a project in mind? I'd love to hear from you!
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a
            href="mailto:dickroldanalambra@gmail.com"
            class="inline-flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700 transition-colors"
          >
            <svg class="mr-2 h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
            Send Email
          </a>
          <a
            href="https://github.com/DickRoldanAlambra"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-flex items-center justify-center px-8 py-3 border border-gray-300 dark:border-gray-600 text-base font-medium rounded-md text-gray-700 dark:text-gray-300 bg-white dark:bg-gray-800 hover:bg-gray-50 dark:hover:bg-gray-700 transition-colors"
          >
            <svg class="mr-2 h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
              <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd" />
            </svg>
            View GitHub
          </a>
          <a
            href="https://linkedin.com/in/dick-alambra-8949a9213"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-flex items-center justify-center px-8 py-3 border border-gray-300 dark:border-gray-600 text-base font-medium rounded-md text-gray-700 dark:text-gray-300 bg-white dark:bg-gray-800 hover:bg-gray-50 dark:hover:bg-gray-700 transition-colors"
          >
            <svg class="mr-2 h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
              <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
            </svg>
            Connect on LinkedIn
          </a>
        </div>
      </div>
    </section>

    <Footer />
  </div>
</template>

<script setup lang="ts">
// SEO
useHead({
  title: 'Dick Roldan Alambra - IT Professional Portfolio',
  meta: [
    { name: 'description', content: 'Information Technology professional specializing in practical, innovative solutions. Building modern web applications that solve real-world problems.' },
    { property: 'og:title', content: 'Dick Roldan Alambra - IT Professional Portfolio' },
    { property: 'og:description', content: 'Information Technology professional specializing in practical, innovative solutions.' }
  ]
})

// Define icon components as simple SVG wrappers
const CodeIcon = {
  template: `
    <svg fill="none" viewBox="0 0 24 24" stroke="currentColor">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
    </svg>
  `
}

const ServerIcon = {
  template: `
    <svg fill="none" viewBox="0 0 24 24" stroke="currentColor">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h14M5 12a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v4a2 2 0 01-2 2M5 12a2 2 0 00-2 2v4a2 2 0 002 2h14a2 2 0 002-2v-4a2 2 0 00-2-2m-2-4h.01M17 16h.01" />
    </svg>
  `
}

const DatabaseIcon = {
  template: `
    <svg fill="none" viewBox="0 0 24 24" stroke="currentColor">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4" />
    </svg>
  `
}

const CloudIcon = {
  template: `
    <svg fill="none" viewBox="0 0 24 24" stroke="currentColor">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z" />
    </svg>
  `
}

const MobileIcon = {
  template: `
    <svg fill="none" viewBox="0 0 24 24" stroke="currentColor">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" />
    </svg>
  `
}

const GitIcon = {
  template: `
    <svg fill="none" viewBox="0 0 24 24" stroke="currentColor">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
    </svg>
  `
}

const skills = [
  {
    icon: CodeIcon,
    title: 'Frontend Development',
    description: 'Vue.js, Nuxt, WinForms, Angular, TypeScript, Tailwind CSS'
  },
  {
    icon: ServerIcon,
    title: 'Backend Development',
    description: 'Node.js, Laravel, PHP, C#, REST APIs'
  },
  {
    icon: DatabaseIcon,
    title: 'Database Management',
    description: 'MSSQL, MySQL'
  },
  {
    icon: GitIcon,
    title: 'Version Control',
    description: 'Git, GitHub, GitLab, Code Review'
  }
]

const projects = [
  {
    title: 'Project One',
    description: 'A modern web application built with cutting-edge technologies.',
    image: 'https://via.placeholder.com/400x300/3B82F6/FFFFFF?text=Project+One',
    tags: ['Vue.js', 'Nuxt', 'TypeScript'],
    link: '#'
  },
  {
    title: 'Project Two',
    description: 'An innovative solution to streamline workflow automation.',
    image: 'https://via.placeholder.com/400x300/3B82F6/FFFFFF?text=Project+Two',
    tags: ['Node.js', 'Express', 'MongoDB'],
    link: '#'
  },
  {
    title: 'Project Three',
    description: 'A mobile-first application with seamless user experience.',
    image: 'https://via.placeholder.com/400x300/3B82F6/FFFFFF?text=Project+Three',
    tags: ['React Native', 'Firebase', 'Redux'],
    link: '#'
  }
]

const handleImageError = (event: Event) => {
  const target = event.target as HTMLImageElement
  target.src = 'https://via.placeholder.com/400x300/3B82F6/FFFFFF?text=Project+Image'
}
</script>
