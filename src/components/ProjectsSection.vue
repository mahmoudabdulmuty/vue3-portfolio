<script setup lang="ts">
interface Project {
  title: string
  description: string
  technologies: string[]
  image: string
  link: string
}

const projects: Project[] = [
  {
    title: 'E-commerce Platform',
    description: 'A modern e-commerce platform built with Vue 3 and Quasar',
    technologies: ['Vue 3', 'TypeScript', 'Quasar', 'Pinia'],
    image: 'https://picsum.photos/600/400',
    link: '#'
  },
  {
    title: 'Task Management App',
    description: 'A collaborative task management application',
    technologies: ['Vue 3', 'Firebase', 'Tailwind CSS'],
    image: 'https://picsum.photos/600/401',
    link: '#'
  },
  {
    title: 'Portfolio Website',
    description: 'A responsive portfolio website template',
    technologies: ['Vue 3', 'Quasar', 'GSAP'],
    image: 'https://picsum.photos/600/402',
    link: '#'
  }
]
</script>

<template>
  <div id="projects" class="q-pa-md">
    <h2 class="text-h3 text-center q-mb-xl">Projects</h2>
    <div class="row q-col-gutter-md">
      <div v-for="project in projects" :key="project.title" class="col-12 col-md-4">
        <q-card class="project-card">
          <q-img :src="project.image" />
          <q-card-section>
            <div class="text-h6">{{ project.title }}</div>
            <p>{{ project.description }}</p>
          </q-card-section>
          <q-card-section>
            <q-chip
              v-for="tech in project.technologies"
              :key="tech"
              color="primary"
              text-color="white"
              class="q-ma-xs"
            >
              {{ tech }}
            </q-chip>
          </q-card-section>
          <q-card-actions align="right">
            <q-btn flat color="primary" :href="project.link" target="_blank" label="View Project" />
          </q-card-actions>
        </q-card>
      </div>
    </div>
  </div>
</template>

<style scoped>
.project-card {
  height: 100%;
  transition: transform 0.2s;
}

.project-card:hover {
  transform: translateY(-5px);
}
</style>