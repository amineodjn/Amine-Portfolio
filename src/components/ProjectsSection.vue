<template>
  <section class="projects">
    <div class="wrapper projects_wrapper">
      <div class="projects_grid">
        <h2 class="projects_headline header-xl">Projects</h2>
        <a href="#contact" class="projects_contact underline">Contact me</a>
        <div class="projects_item">
          <picture class="projects_picture">
            <source media="(min-width: 62.5em)" src="/images/thumbnail-project-1-large.webp">
            <img class="projects_image" src="/images/thumbnail-project-1-small.webp" alt="screenshot of Expense Tracker website" width="343" height="253" />
          </picture> 
          <h3 class="projects_name">Expense Tracker</h3>
          <p class="projects_tags">
            <span>VueJs</span>
            <span>CSS</span>
            <span>echarts</span>
          </p>
          <div class="projects_links">
            <a href="https://main.d20xnln01voqtq.amplifyapp.com/" class="underline">View Project</a>
            <a href="https://github.com/amineodjn/expense-tracker" class="underline">View Code</a>
          </div>   
        </div>
        <div class="projects_item">
          <picture class="projects_picture">
            <source media="(min-width: 62.5em)" srcset="/images/thumbnail-project-2-large.webp">
            <img class="projects_image" src="/images/thumbnail-project-2-small.webp" alt="screenshot of design portfolio website" width="343" height="253" />
          </picture> 
          <h3 class="projects_name">Multicoach</h3>
          <p class="projects_tags">
            <span>VueJS</span>
            <span>Tailwind</span>
            <span>Firebase</span>
            <span>AWS</span>
          </p>
          <div class="projects_links">
            <a href="https://staging.d1m061trrx56au.amplifyapp.com/register-user" class="underline">View Project</a>
            <a href="https://github.com/amineodjn/MultiCoach" class="underline">View Code</a>
          </div>   
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
</script>