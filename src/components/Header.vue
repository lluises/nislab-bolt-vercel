<script setup lang="ts">
const links = [
  { text: 'About Me', href: '#about' },
  { text: 'Projects', href: '#projects' },
  { text: 'Skills', href: '#skills' },
  { text: 'Contact', href: '#contact' }
]
</script>

<template>
  <v-app-bar color="primary" density="compact">
    <v-container class="d-flex align-center">
      <v-toolbar-title class="text-h6">エスカーニョ マルケス ユイス</v-toolbar-title>
      <v-spacer></v-spacer>
      <div class="d-none d-sm-flex">
        <v-btn v-for="link in links" :key="link.text" :href="link.href" variant="text">
          {{ link.text }}
        </v-btn>
      </div>
      <v-app-bar-nav-icon class="d-flex d-sm-none"></v-app-bar-nav-icon>
    </v-container>
  </v-app-bar>
</template>