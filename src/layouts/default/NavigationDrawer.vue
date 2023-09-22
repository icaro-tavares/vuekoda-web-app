<template>
  <v-navigation-drawer app :value="drawer" @input="$emit('update:drawer', $event)">
    <v-list
      :lines="false"
      density="compact"
      nav
    >
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :value="item"
        color="primary"
      >
        <template v-slot:prepend>
          <v-icon :icon="item.icon"></v-icon>
        </template>

        <v-list-item-title v-text="item.text"></v-list-item-title>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  props: {
    drawer: Boolean,
  },
  data: () => ({
    items: [
      { text: 'Início', icon: 'mdi-folder' },
      { text: 'Clientes', icon: 'mdi-account-multiple' },
      { text: 'Propostas', icon: 'mdi-star' },
      { text: 'Recent', icon: 'mdi-history' },
      { text: 'Offline', icon: 'mdi-check-circle' },
      { text: 'Uploads', icon: 'mdi-upload' },
      { text: 'Backups', icon: 'mdi-cloud-upload' },
    ],
  }),
};
</script>
