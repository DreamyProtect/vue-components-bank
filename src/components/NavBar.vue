<template>
  <ul class="flex flex justify-end w-full">
    <li v-for="(navItem, index) in routes"
      :key="index">
      <NavigationElement
        :name="navItem.name"
        :path="navItem.path"/>
    </li>
  </ul>
</template>

<script>
import NavigationElement from '@/components/NavigationElement'
export default {
  name: 'NavBar',
  props: ['routes'],
  components: {
    NavigationElement
  }
}
</script>
