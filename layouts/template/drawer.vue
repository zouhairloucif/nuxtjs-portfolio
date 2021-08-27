<template>
  <v-navigation-drawer color="info lighten-2" :mini-variant="false" app>
    <v-list>
      <v-list-item inactive :ripple="false" nuxt :to="{name: 'about'}">
        <v-list-item-avatar size="180" horizontal class="mx-auto">
          <v-img max-height="200px" :src="imageUrl"></v-img>
        </v-list-item-avatar>
      </v-list-item>
      <v-list-item v-for="(item, i) in items" :key="i" :to="{name: item.to}" router exact dark>
        <v-list-item-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>
            <span class="font-weight-medium">{{ item.title }}</span>
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  data () {
    return {
      imageUrl: "/images/me.jpeg",
      items: [
        {
          icon: 'mdi-account-outline',
          title: 'About',
          to: 'about'
        },
        {
          icon: 'mdi-briefcase-variant-outline',
          title: 'Experience',
          to: 'experience'
        },
        {
          icon: 'mdi-school-outline',
          title: 'Education',
          to: 'education'
        },
        {
          icon: 'mdi-lightbulb-on-outline',
          title: 'Skills',
          to: 'skills'
        },
        {
          icon: 'mdi-star-outline',
          title: 'Interests',
          to: 'interest'
        },
        {
          icon: 'mdi-folder-multiple-outline',
          title: 'Portfolio',
          to: 'portfolio'
        },
        {
          icon: 'mdi-translate',
          title: 'Languages',
          to: 'languages'
        },
        {
          icon: 'mdi-email-send-outline',
          title: 'Contact',
          to: 'contact'
        }
      ],
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
