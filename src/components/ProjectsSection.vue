<template>
  <section class="projects">
    <div class="wrapper projects_wrapper">
      <div class="projects_grid">
        <h2 class="projects_headline header-xl">Projects</h2>
        <a href="#contact" class="projects_contact underline">Contact me</a>
        <div 
          v-for="project in PROJECTS" 
          :key="project.name"
          class="projects_item"
        >
          <picture class="projects_picture">
            <source
              media="(min-width: 62.5em)"
              :src="project.imageLarge"
            />
            <img
              class="projects_image"
              :src="project.imageSmall"
              :alt="project.alt"
              width="343"
              height="253"
            />
          </picture>
          <h3 class="projects_name">{{ project.name }}</h3>
          <p class="projects_tags">
            <span v-for="tag in project.tags" :key="tag">{{ tag }}</span>
          </p>
          <div class="projects_links">
            <a
              v-if="project.projectUrl"
              :href="project.projectUrl"
              class="underline"
              target="_blank"
              >View Project</a
            >
            <a
              :href="project.codeUrl"
              class="underline"
              target="_blank"
              >View Code</a
            >
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const PROJECTS = [
    {
      name: 'Web pos system',
      imageLarge: '/images/thumbnail-project-1-large.webp',
      imageSmall: '/images/thumbnail-project-1-small.webp',
      alt: 'screenshot of design portfolio website',
      tags: ['VueJS', 'Typescript', 'Tailwind', 'Firebase'],
      projectUrl: 'https://web-pos-demo.web.app/admin/dashboard',
      codeUrl: 'https://github.com/amineodjn/web-pos-frontend'
    },
    {
    name: 'Multicoach',
    imageLarge: '/images/thumbnail-project-1-large.webp',
    imageSmall: '/images/thumbnail-project-1-small.webp',
    alt: 'screenshot of design portfolio website',
    tags: ['VueJS', 'Tailwind', 'Firebase', 'AWS'],
    projectUrl: 'https://multicoach-4a815.web.app/',
    codeUrl: 'https://github.com/amineodjn/MultiCoach'
  },
  {
    name: 'Expense Tracker',
    imageLarge: '/images/thumbnail-project-2-large.webp',
    imageSmall: '/images/thumbnail-project-2-small.webp',
    alt: 'screenshot of Expense Tracker website',
    tags: ['VueJs', 'CSS', 'echarts'],
    projectUrl: 'https://main.d2udepy2qu8l7r.amplifyapp.com/',
    codeUrl: 'https://github.com/amineodjn/expense-tracker'
  },
  {
    name: 'DevOps',
    imageLarge: '/images/thumbnail-project-2-large.webp',
    imageSmall: '/images/thumbnail-project-2-small.webp',
    alt: 'screenshot of Expense Tracker website',
    tags: ['AWS', 'K8s', 'Terraform'],
    codeUrl: 'https://github.com/amineodjn/DevOps'
  },
]
</script>
