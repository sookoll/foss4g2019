<template lang='pug'>
#slides
  .eg-slideshow
    slide(enter='fadeIn' leave='bounceOutLeft')
      .center.frontpage
        h1 Eagle.js
        h4 A Slideshow Framework for Vue.js
</template>

<script>
import eagle from 'eagle.js'
export default {
  mixins: [ eagle.slideshow ],
  infos: {
    // These infos appear on the home page, below the slideshow's thumbnail
    title: 'Your First Slideshow',
    description: 'A boilerplate to get you started',
    path: 'your-first-slideshow'
  },
  data () {
    return {
      preloadedImages: {
        computerKid: 'https://i.imgur.com/AAlntwU.gif'
      }
    }
  }
}
</script>

<style lang='scss'>
@import 'node_modules/eagle.js/dist/themes/agrume/agrume';

</style>
