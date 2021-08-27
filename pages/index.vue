<template>
  <v-row justify="center" align="center">
    <v-col cols="12" class="text-center">
      <h1 class="info--text lighten-2">Welcome to my Portfolio</h1>
    </v-col>
  </v-row>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  }
}
</script>
