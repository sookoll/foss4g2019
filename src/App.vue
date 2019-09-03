<template lang='pug'>
#app
  slides
</template>

<script>
import Slides from './Slides'
export default {
  name: 'app',
  components: { Slides }
}
</script>

<style lang="scss">
html, body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

</style>
