<template>
  <div class="about">
    <div id="map"></div>
  </div>
</template>
<script setup>
import L from 'leaflet'
import { onMounted } from 'vue'
onMounted(() => {
  const map = L.map('map').setView([51.505, -0.09], 13)
  L.tileLayer('', {
    maxZoom: 19
  }).addTo(map)
  L.marker([51.5, -0.09]).addTo(map)
})
</script>
<style scoped lang="scss">
#map {
  width: 500px;
  height: 180px;
}
</style>
