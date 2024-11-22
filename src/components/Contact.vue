<script setup lang="ts">
const links = {
  email: "CensoredForPrivacy@example.com",
  github: "https://github.com/lluises/"
}
</script>

<template>
  <section id="contact" class="py-16 bg-grey-lighten-4">
    <v-container>
      <h2 class="text-h4 mb-6">Contact</h2>
      <v-row justify="center">
        <v-col cols="12" md="6">
          <v-list>
            <v-list-item>
              <template v-slot:prepend>
                <v-icon>mdi-email</v-icon>
              </template>
              <v-list-item-title>
                <a :href="'mailto:' + links.email">{{ links.email }}</a>
              </v-list-item-title>
            </v-list-item>
            <v-list-item>
              <template v-slot:prepend>
                <v-icon>mdi-github</v-icon>
              </template>
              <v-list-item-title>
                <a :href="links.github" target="_blank">GitHub Profile</a>
              </v-list-item-title>
            </v-list-item>
          </v-list>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>