<template>
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      app
    >
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>John Leider</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>

        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-bottom-navigation height='40' fixed
    :value="activeBtn"
    color="primary"
    horizontal
  >
    <v-btn>
      <span>Recents</span>
      <v-icon small class='mr-0'>mdi-history</v-icon>
    </v-btn>

    <v-btn>
      <span>Favorites</span>
      <v-icon small class='mr-0'>mdi-heart</v-icon>
    </v-btn>

    <v-btn>
      <span>Nearby</span>
      <v-icon small class='mr-0'>mdi-map-marker</v-icon>
    </v-btn>
  </v-bottom-navigation>
    </v-navigation-drawer>
</template>

<script>
export default {
  computed: {
    drawer: {
      get () {
        return this.$store.state.drawer
      },
      set (val) {
        this.$store.commit('SET_DRAWER', val)
      }
    }
  },
  data () {
    return {
      items: [
        { title: '听歌识曲', icon: 'mdi-account' },
        { title: '演出', icon: 'mdi-car' },
        { title: '商城', icon: 'mdi-account' },
        { title: '附件的人', icon: 'mdi-account' },
        { title: '我的订单', icon: 'mdi-account' },
        { title: '定时停止播放', icon: 'mdi-account' },
        { title: '扫一扫', icon: 'mdi-account' },
        { title: '音乐闹钟', icon: 'mdi-account' },
        { title: '音乐云盘', icon: 'mdi-account' },
        { title: '在线听歌免流量', icon: 'mdi-account' },
        { title: '音乐红包', icon: 'mdi-account' }
      ],
      activeBtn: 1
    }
  }
}
</script>

<style>

</style>
