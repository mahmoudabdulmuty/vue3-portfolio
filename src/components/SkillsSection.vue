<script setup lang="ts">
interface Skill {
  category: string
  items: string[]
}

const skills: Skill[] = [
  {
    category: 'Frontend',
    items: ['Vue.js', 'TypeScript', 'Quasar', 'HTML5', 'CSS3', 'JavaScript']
  },
  {
    category: 'Tools & Methods',
    items: ['Git', 'Webpack', 'Vite', 'Responsive Design', 'Testing']
  },
  {
    category: 'Soft Skills',
    items: ['Problem Solving', 'Team Collaboration', 'Communication', 'Agile']
  }
]
</script>

<template>
  <div class="skills-section q-pa-md bg-grey-2">
    <h2 class="text-h3 text-center q-mb-xl">Skills</h2>
    <div class="row q-col-gutter-md justify-center">
      <div v-for="skill in skills" :key="skill.category" class="col-12 col-md-4">
        <q-card flat bordered>
          <q-card-section>
            <div class="text-h6 text-center q-mb-md">{{ skill.category }}</div>
            <q-list>
              <q-item v-for="item in skill.items" :key="item">
                <q-item-section>
                  <q-item-label>
                    <q-icon name="check" color="primary" /> {{ item }}
                  </q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </div>
</template>

<style scoped>
.skills-section {
  padding: 4rem 0;
}
</style>