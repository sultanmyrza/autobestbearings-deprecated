<template>
  <div>
    <v-btn @click="toggleDarkMode" icon>
      <v-icon>mdi-weather-sunset-down</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  created() {
    if (process.browser) {
      this.$vuetify.theme.dark = localStorage.getItem('darkMode') === 'true'
    }
  },
  methods: {
    toggleDarkMode() {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark
      localStorage.setItem('darkMode', this.$vuetify.theme.dark)
    }
  }
}
</script>
