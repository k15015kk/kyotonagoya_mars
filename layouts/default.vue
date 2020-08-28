<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      clipped
      app
    >
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
    <v-app-bar :clipped-left="clipped" app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }} kyoto.nagoya </span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: true,
      app: true,
      drawer: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Top Page',
          to: '/',
        },
        {
          icon: 'mdi-folder-multiple',
          title: 'Portfolio',
          to: '/',
        },
        {
          icon: 'mdi-account',
          title: 'About Me',
          to: '/',
        },
      ],
      title: 'kyoto.nagoya',
    }
  },
}
</script>
