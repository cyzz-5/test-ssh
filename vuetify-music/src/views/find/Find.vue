<template>
  <v-content class='ma-3'>
    <v-carousel
    cycle
    height="180"
    hide-delimiter-background
    show-arrows-on-hover
  >
    <v-carousel-item
      v-for="(slide, i) in slides"
      :key="i"
    >
      <v-sheet
        :color="colors[i]"
        height="100%"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="display-3">{{ slide }} Slide</div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
  <v-tabs
      v-model="tab"
      grow
    >
      <v-tabs-slider></v-tabs-slider>
      <v-tab
        v-for="i in tabs"
        :key="i"
        :href="`#tab-${i}`"
      >
        {{ i }}
      </v-tab>
      <v-tab-item
        v-for="i in tabs"
        :key="i"
        :value="'tab-' + i"
      >
        <v-card
          flat
          tile
        >
          <v-card-text>haha</v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs>
  </v-content>
</template>

<script>
// import Swiper from '../components/Swiper'
export default {
  components: {
  },
  data () {
    return {
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4'
      ],
      slides: [
        'First',
        'Second',
        'Third',
        'Fourth',
        'Fifth'
      ],
      tab: ['每日推荐', '新歌排行榜', '人气歌单推荐']

    }
  }
}
</script>

<style>

</style>
