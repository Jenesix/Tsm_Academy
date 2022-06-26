<template>
  <v-container>
    <v-carousel class="mt-5">
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
      </v-carousel-item>
    </v-carousel>
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