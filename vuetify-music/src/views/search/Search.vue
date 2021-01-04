<template>
  <v-content  class='pa-3 d-flex' transition="slide-x-transition">
    <div class='d-flex align-center justify-center'>
       <v-icon @click="back">mdi-arrow-left</v-icon>
         <v-text-field
        v-model="songValue"
        placeholder="请输入歌名/歌手"
        class="pa-0 ma-0"
      ></v-text-field>
       <v-icon @click="back">mdi-account</v-icon>
    </div>
    <v-img src="https://picsum.photos/510/300?random" aspect-ratio="1.7"></v-img>
    <v-list  dense>
      <template v-for='(item,index) in items'>
      <v-list-item  :key='item.title'>
        <span class='mr-2'>{{index+1}}</span>
        <v-list-item-content>
        <v-list-item-title two-line>{{item.title}}</v-list-item-title>
         <v-list-item-subtitle>
          {{item.desc}}
        </v-list-item-subtitle>
        </v-list-item-content>
         <v-list-item-action>
            <v-list-item-action-text v-text="item.playVolume"></v-list-item-action-text>
          </v-list-item-action>
      </v-list-item>
      <v-divider v-if="index + 1 < items.length"
            :key="index"></v-divider>
      </template>
    </v-list>
  </v-content>
</template>

<script>
export default {
  name: 'Search',
  data () {
    return {
      songValue: '',
      items: [
        {
          title: 'twice',
          desc: '是否能接受twice的邀请，YES OR YES!',
          playVolume: 59333
        },
        {
          title: 'one',
          desc: '是否能接受twice的邀请，YES OR YES!',
          playVolume: 59333
        },
        {
          title: 'two',
          desc: '是否能接受twice的邀请，YES OR YES!',
          playVolume: 59333
        },
        {
          title: 'three',
          desc: '是否能接受twice的邀请，YES OR YES!',
          playVolume: 59333
        }
      ]
    }
  },
  methods: {
    back () {
      this.$router.go(-1)
    }
  }
}
</script>

<style>

</style>
