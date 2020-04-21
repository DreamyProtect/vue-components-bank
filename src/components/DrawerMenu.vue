<template>
  <div>
    <div :class="{
      'w-4/5': true,
      'hidden': !burgerMenuOpen,
      'h-full fixed bg-red-100': burgerMenuOpen
      }">
      <button
        class="flex w-full justify-end p-5 text-red-500"
        @click="burgerMenuOpen=!burgerMenuOpen"
      >
        <svg class="fill-current h-3 w-3" enable-background="new 0 0 492 492" version="1.1" viewBox="0 0 492 492" xml:space="preserve" xmlns="http://www.w3.org/2000/svg"><path d="m300.19 246 183.95-183.96c5.06-5.064 7.852-11.82 7.86-19.024 0-7.208-2.792-13.972-7.86-19.028l-16.12-16.116c-5.068-5.076-11.824-7.856-19.036-7.856-7.2 0-13.956 2.78-19.024 7.856l-183.95 183.95-183.96-183.95c-5.06-5.076-11.82-7.856-19.028-7.856-7.2 0-13.96 2.78-19.02 7.856l-16.128 16.116c-10.496 10.496-10.496 27.568 0 38.052l183.96 183.96-183.96 183.95c-5.064 5.072-7.852 11.828-7.852 19.032s2.788 13.96 7.852 19.028l16.124 16.116c5.06 5.072 11.824 7.856 19.02 7.856 7.208 0 13.968-2.784 19.028-7.856l183.96-183.95 183.95 183.95c5.068 5.072 11.824 7.856 19.024 7.856h8e-3c7.204 0 13.96-2.784 19.028-7.856l16.12-16.116c5.06-5.064 7.852-11.824 7.852-19.028s-2.792-13.96-7.852-19.028l-183.95-183.96z"/></svg>
      </button>
      <NavigationElement
        v-for="(navItem, index) in routes"
        :key="index"
        :name="navItem.name"
        :path="navItem.path"/>
    </div>
    <div class="justify-start w-1/5">
      <button
        class="flex items-center px-3 py-2 border rounded text-red-200 border-red-400 hover:text-red-500 hover:border-red-500"
        @click="burgerMenuOpen=!burgerMenuOpen"
      >
        <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
      </button>
    </div>
  </div>
</template>

<script>
import NavigationElement from '@/components/NavigationElement'
export default {
  name: 'DrawerMenu',
  props: ['routes'],
  data () {
    return {
      burgerMenuOpen: false
    }
  },
  components: {
    NavigationElement
  }
}
</script>
