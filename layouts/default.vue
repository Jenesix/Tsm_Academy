<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
          class="yellow--text text--darken-3"
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
    <v-app-bar
      class="yellow--text text--darken-3"
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon class="yellow--text text--darken-3"
          >mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon
        >
      </v-btn>
      <v-app-bar-title>Title</v-app-bar-title>

      <v-spacer></v-spacer>
      <div>
        <v-btn text> Test1 </v-btn>

        <v-btn text> Test2 </v-btn>

        <v-btn text> Test3 </v-btn>
        <v-btn text> Test4 </v-btn>
        <v-btn text> Test5 </v-btn>
      </div>
    </v-app-bar>
    <Nuxt />
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
        {
          icon: 'mdi-apps',
          title: 'Slider',
          to: '/slider',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'TSM_Academy',
    }
  },
}
</script>
