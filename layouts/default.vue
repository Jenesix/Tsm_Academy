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
      miniVariant: false,
    }
  },
}
</script>
