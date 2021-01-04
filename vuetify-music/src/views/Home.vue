<template>
  <div class="home" transition="slide-x-reverse-transition">
    <Nav />
    <SideBar/>
    <router-view></router-view>
  </div>
</template>

<script>
// @ is an alias to /src
import Nav from '@/components/Nav.vue'
import SideBar from '@/components/SideBar.vue'
export default {
  name: 'Home',
  components: {
    Nav,
    SideBar
  }
}
</script>
