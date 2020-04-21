<template>
  <div>
    <ul class="flex justify-end w-full">
      <li v-for="(navItem, index) in routes"
        :key="index">
        <NavBarNavigationElement
          :name="navItem.name"
          :path="navItem.path"/>
      </li>
    </ul>
  </div>
</template>

<script>
import NavBarNavigationElement from '@/components/NavBarNavigationElement'
export default {
  name: 'NavBar',
  props: ['routes'],
  components: {
    NavBarNavigationElement
  }
}
</script>
