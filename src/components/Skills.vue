<script setup lang="ts">
const skills = {
  'Front-end': ['HTML', 'CSS', 'JavaScript', 'Vue', 'Vuetify', 'Vite'],
  'Back-end': ['Node.js', 'Python', 'SQL', 'ElasticSearch'],
  'Tools': ['Git', 'Docker', 'GitHub'],
  'Others': ['GNU Emacs']
}
</script>

<template>
  <section id="skills" class="py-16">
    <v-container>
      <h2 class="text-h4 mb-6">Skills</h2>
      <v-row>
        <v-col v-for="(items, category) in skills" :key="category" cols="12" sm="6" md="3">
          <v-card>
            <v-card-title>{{ category }}</v-card-title>
            <v-card-text>
              <v-chip-group>
                <v-chip v-for="skill in items" :key="skill">{{ skill }}</v-chip>
              </v-chip-group>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>