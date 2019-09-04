<template lang='pug'>
#slides.eg-theme-agrume
  .eg-slideshow
    slide(enter='fadeIn' leave='bounceOutLeft')
      h1 FOSS4G 2019
      h3 Bucharest 26 - 30 August 2019
      .center
        i.
          You are awesome, your software is awesome, (but) your software is useless,
      .center
        i.
          ...without data.
    slide.local-theme.bucharest(enter='fadeIn' leave='fadeOut')
    slide.local-theme.foss4g(enter='fadeIn' leave='fadeOut')
    slide(:steps=3 enter='bounceInRight' leave='bounceOutLeft')
      h3 FOSS4G in numbers
      p  42 practical workshops
      p  7 labs
      p  298 talks (1 from Estonia) in 11 parallel sessions, all streamed on live and recorded
      p  9 keynote talks
      p  B2B and BoF meetings, code sprints
      p  1020+ participants around the world (12 from Estonia)
      p(v-if='step > 1') All-inclusive Ice braker party and Gala dinner :)
      p(v-if='step > 2') Pub-race every night :D
    slide.local-theme.icebreaker(enter='fadeIn' leave='fadeOut')
    slide.local-theme.parliament(enter='fadeIn' leave='fadeOut')
    slide.local-theme.pubrace(enter='fadeIn' leave='fadeOut')
    slide(:steps=5 enter='bounceInRight' leave='bounceOutLeft')
      h3 Hot topics
      div(v-if='step > 1' enter='fadeIn' leave='fadeOut')
        eg-code-block(lang='html').
          const awsomeGeoSoftwares = [
            'PostGIS',
            'MapServer',
            'GeoServer',
            'OpenLayers',
            'QGIS',
            'GRASS GIS',
            'GDAL',
            'GeoEXT'
          ]
          awsomeGeoSoftwares.forEach(awsome => {
            console.log("State of " + awsome)
          })
      div(v-if='step > 2' enter='fadeIn' leave='fadeOut')
        p 3D rendering in desktop, web, mobile
      div(v-if='step > 3' enter='fadeIn' leave='fadeOut')
        p WebGL and rendering multi-GB imagery in a browser
      div(v-if='step > 4' enter='fadeIn' leave='fadeOut')
        p (GPU) (real-time) Processing pointclouds and satellite (Sentinel) imagery
    slide.local-theme.weirdstuff(enter='fadeIn' leave='fadeOut')
    slide(enter='bounceInRight' leave='bounceOutLeft')
      h3 Workshops
      h4 Robosat.pink
      p  Detect OSM missing buildings from imagery with deep learning computer vision
    slide.local-theme.workshop(enter='fadeIn' leave='fadeOut')
    slide(enter='bounceInRight' leave='bounceOutLeft')
      h3 Workshops
      h4 R for Geospatial Processing
      p  Spatial data processing and rendering results (maps) with R
    slide(enter='bounceInRight' leave='bounceOutLeft')
      h3 Talks
      p  New features of libraries
      p  Demos of services and softwares
      p  Usecases
      p 11 parallel sessions, so got covered less than 10%
    slide.local-theme.talk(enter='fadeIn' leave='fadeOut')
    slide(enter='bounceInRight' leave='bounceOutLeft')
      h3 GeoStuff
      p https://2019.foss4g.org
      p https://media.ccc.de/c/foss4g2019
      p https://www.osgeo.org
      p http://www.opengeospatial.org
    slide.local-theme.cat(enter='fadeIn' leave='fadeOut')

</template>

<script>
import eagle from 'eagle.js'
export default {
  mixins: [ eagle.slideshow ],
  data () {
    return {
      preloadedImages: {}
    }
  }
}
</script>

<style lang='scss'>
@import 'node_modules/eagle.js/dist/themes/agrume/agrume';
.pad {
  padding: 0.5rem
}
.local-theme {
  background-position: center;
  background-size: cover;
  color: white;
  &.bucharest {
    background-image: url(https://i.imgur.com/8gq7JZm.jpg);
  }
  &.foss4g {
    background-image: url(https://i.imgur.com/X5TZUPR.jpg);
  }
  &.icebreaker {
    background-image: url(https://i.imgur.com/7785unD.jpg);
  }
  &.parliament {
    background-image: url(https://i.imgur.com/uNlPztT.jpg);
  }
  &.pubrace {
    background-image: url(https://i.imgur.com/IVJYQNB.jpg);
  }
  &.weirdstuff {
    background-image: url(https://i.imgur.com/W3mxDrO.jpg);
  }
  &.workshop {
    background-image: url(https://i.imgur.com/oZN6kUp.jpg);
  }
  &.talk {
    background-image: url(https://i.imgur.com/wGIhbYw.jpg);
  }
  &.cat {
    background-image: url(https://i.imgur.com/GfHljbv.jpg);
  }
}

</style>
