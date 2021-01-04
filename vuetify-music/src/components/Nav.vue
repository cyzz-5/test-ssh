<template>
   <v-app-bar id='app-bar' color='white' app dense  absolute flat fixed>
    <v-app-bar-nav-icon @click="setDrawer(!drawer)"></v-app-bar-nav-icon>
    <v-spacer></v-spacer>
    <v-btn text @click="myClick">我的</v-btn>
    <v-btn text @click='findClick'>发现</v-btn>
    <v-spacer></v-spacer>
    <v-btn icon to='/search'>
      <v-icon>mdi-magnify</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script>
import { mapState, mapMutations } from 'vuex'
export default {
  data () {
    return {
    }
  },
  computed: {
    ...mapState(['drawer'])
  },
  methods: {
    ...mapMutations({ setDrawer: 'SET_DRAWER' }),
    myClick () {},
    findClick () {
      this.$router.push('/find')
    }
  }
}
</script>

<style>

</style>
