<template lang='pug'>
#slides.eg-theme-agrume
  .eg-slideshow
    slide.local-theme.bucharest(enter='fadeIn' leave='bounceOutLeft')
      h2 FOSS4G 2019
      h4.center Bucharest 26 - 30 August 2019
      .center.quote
        div
          i You are awesome, your software is awesome
        div
          i (but) your software is useless
        div
          i ...without data
    slide(enter='bounceInRight' leave='bounceOutLeft')
      h3 FOSS4G
      p  ...stands for Free and Open Source Software for Geospatial
      p  ...is hosted by OSGeo (Open Source Geospatial Foundation)
      p  ...is the largest global gathering focused on open source geospatial software.
    slide.local-theme.foss4g(enter='fadeIn' leave='fadeOut')
    slide(:steps=3 enter='bounceInRight' leave='bounceOutLeft')
      h3 FOSS4G in numbers
      p  42 practical workshops
      p  7 labs
      p  298 talks (1 from Estonia) in 11 parallel sessions, all streamed on live and recorded
      p  9 keynote talks
      p  B2B and BoF meetings, code sprints
      p  1020+ participants around the world (12 from Estonia)
      p.strong(v-if='step > 1') All-inclusive Ice breaker party and Gala dinner :)
      p.strong(v-if='step > 2') Pub-race every night :D
    slide.local-theme.icebreaker(enter='fadeIn' leave='fadeOut')
    slide.local-theme.parliament(enter='fadeIn' leave='fadeOut')
    slide.local-theme.pubrace(enter='fadeIn' leave='fadeOut')
    slide(:steps=4 enter='bounceInRight' leave='bounceOutLeft')
      h3 Hot topics
      div(v-if='step > 1' enter='fadeIn' leave='fadeOut')
        p (3D) Vector tiles
      div(v-if='step > 2' enter='fadeIn' leave='fadeOut')
        p WebGL and rendering multi-GB imagery in a browser
      div(v-if='step > 3' enter='fadeIn' leave='fadeOut')
        p (GPU) (real-time) processing big-data, pointclouds and satellite (Sentinel) imagery
    slide.local-theme.talk3(enter='fadeIn' leave='fadeOut')
    slide(enter='bounceInRight' leave='bounceOutLeft')
      h3 Workshops
      h4 Robosat.pink
      p  Detect OSM missing buildings from imagery with deep learning computer vision
    slide.local-theme.workshop(enter='fadeIn' leave='fadeOut')
    slide(enter='bounceInRight' leave='bounceOutLeft')
      h3 Workshops
      h4 R for Geospatial Processing
      p  Spatial data processing and rendering results (maps) with R
    slide(:steps=6 enter='bounceInRight' leave='bounceOutLeft')
      h3 Talks
      div(v-if='step > 1' enter='fadeIn' leave='fadeOut')
        eg-code-block.codeblock(lang='html').
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
      p(v-if='step > 2')  New features of libraries
      p(v-if='step > 3')  Demos of services and softwares
      p(v-if='step > 4')  Usecases
      p(v-if='step > 5') 11 parallel sessions, so got covered less than 10%
    slide.local-theme.talk(enter='fadeIn' leave='fadeOut')
    slide.local-theme.talk2(enter='fadeIn' leave='fadeOut')
    slide(enter='bounceInRight' leave='bounceOutLeft')
      h3 New innovative ideas
      p Using Cloud Optimised GeoTiffs to Query 24 Billion Pixels In Real-Time
      p geotiff.js
      p GPU-based neurals network processing
    slide.local-theme.weirdstuff(enter='fadeIn' leave='fadeOut')
    slide(enter='bounceInRight' leave='bounceOutLeft')
      h3 GeoStuff
      p
        a(href='https://2019.foss4g.org' target='_blank') https://2019.foss4g.org
      p
        a(href='https://media.ccc.de/c/foss4g2019' target='_blank') https://media.ccc.de/c/foss4g2019
      p
        a(href='https://www.osgeo.org' target='_blank') https://www.osgeo.org
      p
        a(href='https://www.opengeospatial.org' target='_blank') https://www.opengeospatial.org
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
.strong {
  font-weight: bold!important
}
.codeblock .code-box {
  box-shadow: none;
  border: 1px solid #ddd
}
.quote {
  font-family: "Pompiere", cursive
}
.local-theme {
  background-position: center center;
  background-size: cover;
  color: white;
  &.bucharest {
    background: linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.8)), url(https://2019.foss4g.org/wp-content/uploads/2018/07/cover-1-logo.jpg);
    background-position: -100px center;
    h2 {
      padding-top: 30%
    }
  }
  &.foss4g {
    background-image: url(https://i.imgur.com/X5TZUPR.jpg)
  }
  &.icebreaker {
    background-image: url(https://i.imgur.com/7785unD.jpg)
  }
  &.parliament {
    background-image: url(https://i.imgur.com/uNlPztT.jpg)
  }
  &.pubrace {
    background-image: url(https://i.imgur.com/IVJYQNB.jpg)
  }
  &.weirdstuff {
    background-image: url(https://i.imgur.com/W3mxDrO.jpg)
  }
  &.workshop {
    background-image: url(https://i.imgur.com/oZN6kUp.jpg)
  }
  &.talk {
    background-image: url(https://i.imgur.com/wGIhbYw.jpg)
  }
  &.talk2 {
    background-image: url(https://i.imgur.com/AkXrfld.png)
  }
  &.cat {
    background-image: url(https://i.imgur.com/GfHljbv.jpg)
  }
  &.talk3 {
    background-image: url(https://i.imgur.com/2wwRmvm.png)
  }
}

</style>
