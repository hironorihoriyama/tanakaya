<template>
  <GmapMap
    map-type-id="roadmap"
    :center="center"
    :zoom="15"
    :options="options.map"
  >
  </GmapMap>
</template>

<script>
export default {
  data: function() {
    return {
      center: {
        lat: 34.5306955,
        lng: 135.9063403
      },
      infos: {
        pos: null,
        open: false,
      },
      options: {
        map: {
          zoomControl: false,
          mapTypeControl: false,
          streetViewControl: false,
          fullscreenControl: false
        }
      }
    }
  },
}
</script>

<style lang="sass">
.vue-map-container
  width: 100%
  height: 589px
</style>