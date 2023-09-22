<template>
  <div class="auth-wrapper auth bg-grey-lighten-5">
    <div class="auth-inner">
      <v-img
        class="mx-auto my-6"
        max-width="228"
        src="https://cdn.vuetifyjs.com/docs/images/logos/vuetify-logo-v3-slim-text-light.svg"
      ></v-img>

      <v-card
        class="pa-12 pb-8"
        elevation="5"
      >
        <div class="text-subtitle-1 text-medium-emphasis">{{ emailLabel }}</div>

        <v-text-field
          density="compact"
          :placeholder="emailPlaceholder"
          prepend-inner-icon="mdi-email-outline"
          variant="outlined"
        ></v-text-field>

        <div class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between">
          {{ passwordLabel }}

          <a
            class="text-caption text-decoration-none text-blue"
            href="#"
            rel="noopener noreferrer"
            target="_blank"
          >
            {{ forgotPasswordText }}
          </a>
        </div>

        <v-text-field
          :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
          :type="visible ? 'text' : 'password'"
          density="compact"
          placeholder="********"
          prepend-inner-icon="mdi-lock-outline"
          variant="outlined"
          @click:append-inner="visible = !visible"
        ></v-text-field>

        <v-btn
          block
          class="mb-6"
          color="primary"
          size="large"
          variant="tonal"
        >
          {{ loginButtonText }}
        </v-btn>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false,
      emailLabel: 'E-mail',
      emailPlaceholder: 'me@icarotavares.com',
      passwordLabel: 'Senha',
      forgotPasswordText: 'Esqueceu sua senha?',
      loginButtonText: 'Entrar',
    };
  },
};
</script>

<style lang="scss">
@import '@/assets/scss/auth.scss';
</style>
