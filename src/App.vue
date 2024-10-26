<script setup lang="ts">
import HeroSection from './components/HeroSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ContactSection from './components/ContactSection.vue'
</script>

<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title>Portfolio</q-toolbar-title>
        <q-space />
        <div class="q-gutter-sm">
          <q-btn flat dense href="#" label="Home" />
          <q-btn flat dense href="#projects" label="Projects" />
          <q-btn flat dense href="#contact" label="Contact" />
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <q-page>
        <HeroSection />
        <ProjectsSection />
        <SkillsSection />
        <ContactSection id="contact" />
      </q-page>
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title class="text-center">
          © {{ new Date().getFullYear() }} - Created with Vue 3 & Quasar
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<style>
body {
  margin: 0;
  padding: 0;
}
</style>