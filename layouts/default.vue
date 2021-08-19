<template>
  <v-app dark>
    <drawer/>
    <v-main>
      <v-container>
        <div class="text-right px-4">
          <v-btn elevation="0" :ripple="false" @click="toggleDarkTheme" plain fab class="darkMode">
            <v-icon :class="{'active': isDarkTheme, 'unactive': !isDarkTheme}">{{ isDarkTheme ? 'mdi-brightness-4' : 'mdi-brightness-6' }}</v-icon>
          </v-btn>
        </div>
        <v-container>
          <transition name="fade" mode="out-in">
            <nuxt/>
          </transition>
        </v-container>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import drawer from "~/layouts/template/drawer";

export default {
  components: {
    drawer,
  },
  computed: {
    isDarkTheme() {
      return this.$vuetify.theme.dark;
    },
  },
  methods: {
    toggleDarkTheme() {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark;
    },
  },
}
</script>

<style lang="scss" scoped>
.darkMode {
  transition: transform 1s;
  .active {
    transform: rotateZ(-180deg);
  }
  .unactive {
    transform: rotateZ(180deg);
  }
}
</style>
