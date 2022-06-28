<template>
  <v-container>
    <v-carousel class="mt-12 pt-12">
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
      </v-carousel-item>
    </v-carousel>
    <v-container>
      <div>
        <v-row justify="center" align="center">
          <v-col cols="11" class="mt-8"
            ><v-btn class="mr-10" height="40%" width="20%" to="/dance"
              ><v-card height="200px"></v-card>
            </v-btn>
            <v-btn class="ma-10" height="40%" width="20%"
              ><v-card height="200px"></v-card>
            </v-btn>
            <v-btn class="ma-10" height="40%" width="20%"
              ><v-card height="200px"></v-card>
            </v-btn>
            <v-btn class="ma-10" height="40%" width="20%"
              ><v-card height="200px"></v-card> </v-btn></v-col
        ></v-row>
      </div>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: 'SliderPage',

  data() {
    return {
      items: [
        {
          src: '/picture/test.jpg',
        },
        {
          src: '/picture/test1.jpg',
        },
        {
          src: '/picture/test2.jpg',
        },
      ],
    }
  },
}
</script>

<style>
</style>