<script setup lang="ts">
import NeshanMap from "@neshan-maps-platform/vue3-openlayers"
import { ref, watch } from "vue"
const mapKey = "Your_Map_KEY"
const serviceKey = "Your_SERVICE_KEY"
const mapRef = ref<InstanceType<typeof NeshanMap>>()
watch(
  () => mapRef.value?.state.map,
  (nv, ol) => {
    if (ol) return
    setTimeout(() => {
      mapRef.value?.state.map?.setMapType("standard-night")
      if (mapRef.value?.state.mapType)
        mapRef.value.state.mapType = "standard-night"
    }, 2000)
    setTimeout(() => {
      mapRef.value?.search({
        term: "ولی عصر",
        coords: [51.36281969540723, 35.69672648316882],
      })
    }, 3000)
  }
)
</script>

<template>
  <NeshanMap
    ref="mapRef"
    :mapKey="mapKey"
    :serviceKey="serviceKey"
    :center="{ latitude: 35.69672648316882, longitude: 51.36281969540723 }"
    :zoom="12"
    class="map"
    :scale="0.8"
  />
</template>

<style>
html,
body,
#app {
  width: 100vw;
  height: 100vh;
  margin: 0;
}
#app {
  display: flex;
}
.map {
  width: 80% !important;
  height: 80% !important;
  margin: auto;
}
</style>
