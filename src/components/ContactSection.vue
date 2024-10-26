<script setup lang="ts">
const contactInfo = {
  email: 'john.doe@example.com',
  github: 'https://github.com/johndoe',
  linkedin: 'https://linkedin.com/in/johndoe'
}
</script>

<template>
  <div class="contact-section q-pa-md">
    <h2 class="text-h3 text-center q-mb-xl">Contact</h2>
    <div class="row justify-center">
      <div class="col-12 col-md-6 text-center">
        <q-list>
          <q-item clickable tag="a" :href="`mailto:${contactInfo.email}`">
            <q-item-section avatar>
              <q-icon name="email" color="primary" size="md" />
            </q-item-section>
            <q-item-section>{{ contactInfo.email }}</q-item-section>
          </q-item>
          
          <q-item clickable tag="a" :href="contactInfo.github" target="_blank">
            <q-item-section avatar>
              <q-icon name="code" color="primary" size="md" />
            </q-item-section>
            <q-item-section>GitHub</q-item-section>
          </q-item>
          
          <q-item clickable tag="a" :href="contactInfo.linkedin" target="_blank">
            <q-item-section avatar>
              <q-icon name="work" color="primary" size="md" />
            </q-item-section>
            <q-item-section>LinkedIn</q-item-section>
          </q-item>
        </q-list>
      </div>
    </div>
  </div>
</template>

<style scoped>
.contact-section {
  padding: 4rem 0;
}
</style>