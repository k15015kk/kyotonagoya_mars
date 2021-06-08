<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" fixed temporary app>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar fixed app dense>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <nuxt />
    </v-main>
    <v-footer fixed app>
      <span>&copy; {{ new Date().getFullYear() }} kyoto.nagoya</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: null,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Top Page',
          to: '/',
        },
        {
          icon: 'mdi-folder-multiple',
          title: 'Portfolio',
          to: '/portfolio',
        },
        {
          icon: 'mdi-account',
          title: 'About Me',
          to: '/aboutme',
        },
      ],
      title: 'kyoto.nagoya',
    }
  },
}
</script>
