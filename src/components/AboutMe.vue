<script setup lang="ts">
const expertise = "Full-stack developer, fluent in backend and frontend web technologies"
const background = "I'm a hobbist programer who has been building software solutions since I was 15."
const experience = [
  {
    title: "Full-stack wed developer",
    position: "Software Engineer",
    description: "Full-stack web develoment of quanlity managment SAAS",
    company: "MyCompany1_censored_for_privacy"
  },
  {
    title: "Software developer",
    position: "Software Engineer",
    description: "Developing software for Big Data analisis",
    company: "MyCompany2_censored_for_privacy"
  }
]
</script>

<template>
  <section id="about" class="py-16">
    <v-container>
      <h2 class="text-h4 mb-6">About Me</h2>
      <v-row>
        <v-col cols="12" md="6">
          <p class="text-body-1 mb-4">{{ expertise }}</p>
          <p class="text-body-1 mb-6">{{ background }}</p>
        </v-col>
        <v-col cols="12" md="6">
          <h3 class="text-h5 mb-4">Experience</h3>
          <v-timeline>
            <v-timeline-item v-for="job in experience" :key="job.title">
              <template v-slot:title>
                <h4 class="text-h6">{{ job.title }}</h4>
                <p class="text-subtitle-1">{{ job.position }} at {{ job.company }}</p>
              </template>
              <p>{{ job.description }}</p>
            </v-timeline-item>
          </v-timeline>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>