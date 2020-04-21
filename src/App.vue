<template>
  <div id="app">
    <DrawerMenu
      class="flex lg:hidden"
      :routes="routesForNav"
    />
    <NavBar
      class="lg:flex hidden lg:bg-gray-500"
      :routes="routesForNav"
    />
    <router-view/>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import DrawerMenu from '@/components/DrawerMenu.vue'

import '@/assets/css/tailwind.css'
export default {
  name: 'App',
  components: {
    NavBar,
    DrawerMenu
  },
  computed: {
    routesForNav () {
      return this.$router.options.routes
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
