<script setup lang="ts">
import Header from './components/Header.vue'
import AboutMe from './components/AboutMe.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'
</script>

<template>
  <v-app>
    <Header />
    <v-main>
      <AboutMe />
      <Projects />
      <Skills />
      <Contact />
    </v-main>
  </v-app>
</template>