<template>
    <div class="flex m-1">
      <router-link :to="path">{{ name }}</router-link>
    </div>
</template>

<script>
export default {
  name: 'NavBarNavigationElement',
  props: [
    'name',
    'path'
  ]
}
</script>
