<script setup lang="ts">
const personalInfo = {
  name: 'John Doe',
  title: 'Frontend Developer',
  description: 'Passionate about creating beautiful and performant web applications using Vue.js and modern technologies.'
}
</script>

<template>
  <div class="hero-section q-pa-md">
    <div class="row items-center justify-center">
      <div class="col-12 col-md-8 text-center q-pa-xl">
        <h1 class="text-h2 text-weight-bold q-mb-md">{{ personalInfo.name }}</h1>
        <h2 class="text-h4 text-primary q-mb-lg">{{ personalInfo.title }}</h2>
        <p class="text-h6">{{ personalInfo.description }}</p>
        <q-btn
          color="primary"
          label="View Projects"
          class="q-mt-lg"
          size="lg"
          href="#projects"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-section {
  min-height: 100vh;
  display: flex;
  align-items: center;
}
</style>