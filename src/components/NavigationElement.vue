<template>
    <div class="m-1">
      <router-link :to="path">{{ name }}</router-link>
    </div>
</template>

<script>
export default {
  name: 'NavigationElement',
  props: [
    'name',
    'path'
  ]
}
</script>
