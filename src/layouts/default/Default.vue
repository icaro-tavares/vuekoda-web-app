<template>
  <v-app>
    <app-bar @toggle-drawer="toggleDrawer"></app-bar>
    <v-main>
      <default-view />
    </v-main>
    <navigation-drawer v-model="drawer"></navigation-drawer>
  </v-app>
</template>

<script>
import AppBar from "./AppBar.vue";
import DefaultView from './View.vue'
import NavigationDrawer from "./NavigationDrawer.vue";

export default {
  components: {
    AppBar,
    DefaultView,
    NavigationDrawer,
  },
  data() {
    return {
      drawer: false,
    };
  },
  methods: {
    toggleDrawer() {
      this.drawer = !this.drawer;
    },
  },
};

</script>
