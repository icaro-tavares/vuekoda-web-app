<template>
  <v-app-bar
    color="primary"
    density="compact"
  >
    <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>
    <v-app-bar-title>Web App</v-app-bar-title>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    toggleDrawer() {
      this.$emit("toggle-drawer");
    },
  },
};
</script>
