<template>
  <section class="skills">
    <div class="wrapper skills_wrapper bottom-border">
      <h2 class="visually-hidden">Skills</h2>
      <div 
        v-for="skill in skills" 
        :key="skill"
        class="skills_item"
      >
        <h3 class="skills_title">{{ skill }}</h3>
      </div>
    </div>
    <img
      class="skills_rings"
      src="/images/pattern-rings.svg"
      alt=""
      width="530"
      height="129"
    />
  </section>
</template>

<script setup>
const skills = [
  'VueJs',
  'Tailwind CSS',
  'Typescript',
  'Vitest',
  'Jest',
  'i18n',
  'AWS Services',
  'Firebase',
  'DevOps Basics'
]
</script>
