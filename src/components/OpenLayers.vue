<template>
  <div>
    <h1>OpenLayers showing IISc in OpenStreetMaps</h1>
    <div id="map" class="map"></div>
  </div>
</template>

<script>
import ol from 'openlayers';

const drawMap = () => {
  /* eslint-disable no-new */
  new ol.Map({
    target: 'map',
    layers: [
      new ol.layer.Tile({
        source: new ol.source.OSM(),
      }),
    ],
    view: new ol.View({
      center: ol.proj.fromLonLat([77.568340, 13.013510]),
      zoom: 18,
    }),
  });
};

export default {
  mounted() {
    // console.log('calling drawMap now!');
    drawMap();
  },
};
</script>

<style src="openlayers/dist/ol.css"></style>
<style>
.map {
  height: 400px;
  width: 100%;
}
</style>
