<script setup lang="ts">
import { onMounted } from 'vue';
import * as Cesium from '@/cesiumSource'
import './cesiumSource/packages/widgets/Source/widgets.css'
(window as any).CESIUM_BASE_URL = '/cesiumAssets'

function adjustInfoBox() {
  var iframe = document.getElementsByClassName('cesium-infoBox-iframe')[0]
  iframe.setAttribute('sandbox', 'allow-same-origin allow-scripts allow-popups allow-forms')
  iframe.setAttribute('src', '')
}

onMounted(() => {
  // adjustInfoBox()
  const viewer = new Cesium.Viewer('cesiumContainer')
})
</script>

<template>
  <div id="cesiumContainer"></div>
</template>

<style scoped>
#cesiumContainer {
  position: absolute;
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  border: 0px!important;
}
</style>
