<script setup lang="ts">
const projects = [
  {
    name: "Space invaders",
    description: "Space invaders videogame in plain WebGL",
    github: "https://github.com/lluises/space-invaders-webgl/",
    live: "https://lluises.github.io/space-invaders-webgl/",
    image: "https://static1.thegamerimages.com/wordpress/wp-content/uploads/2019/11/space-invaders-feature.jpg"
  }
]
</script>

<template>
  <section id="projects" class="py-16 bg-grey-lighten-4">
    <v-container>
      <h2 class="text-h4 mb-6">Projects</h2>
      <v-row>
        <v-col v-for="project in projects" :key="project.name" cols="12" md="6">
          <v-card>
            <v-img :src="project.image" height="200" cover></v-img>
            <v-card-title>{{ project.name }}</v-card-title>
            <v-card-text>{{ project.description }}</v-card-text>
            <v-card-actions>
              <v-btn :href="project.github" target="_blank" variant="text">
                <v-icon>mdi-github</v-icon> GitHub
              </v-btn>
              <v-btn :href="project.live" target="_blank" variant="text">
                <v-icon>mdi-web</v-icon> Live Demo
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>