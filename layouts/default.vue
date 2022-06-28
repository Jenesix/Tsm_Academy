<template>
  <v-app dark>
    <v-app-bar
      class="yellow--text text--darken-3"
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-title> Title</v-app-bar-title>
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
          title: 'Dance',
          to: '/dance',
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
