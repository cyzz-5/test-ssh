<template>
  <div class='swiper-wrapper'>
     <div class="swiper-slide" :key="banner" v-for="banner in banners">
        <v-card
    class="mx-auto"
    max-width="400"
  >
    <v-img
      class="white--text align-end"
      height="200px"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    >
      <v-card-title>Top 10 Australian beaches</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-0">Number 10</v-card-subtitle>

    <v-card-text class="text--primary">
      <div>Whitehaven Beach</div>

      <div>{{banner}}</div>
    </v-card-text>
  </v-card>
      </div>
  </div>
</template>

<script>
import 'swiper/css/swiper.css'
export default {
  name: 'Swiper',
  components: {

  },
  data () {
    return {
      banners: [1, 2, 3]
    }
  }
}
</script>

<style>

</style>
