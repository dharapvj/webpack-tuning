<template>
  <div>
    <h1>OpenLayers showing IISc in OpenStreetMaps</h1>
    <div id="map" class="map"></div>
  </div>
</template>

<script>
// improvement: load only what you need from openlayers (ol for es2015)
// import ol from 'openlayers';
import TileLayer from 'ol/layer/tile';
import Map from 'ol/map';
import View from 'ol/view';
import OSM from 'ol/source/osm';
import proj from 'ol/proj';

const iiscLocation = proj.fromLonLat([77.568340, 13.013510]);

const drawMap = () => {
  /* eslint-disable no-new */
  new Map({
    target: 'map',
    layers: [
      new TileLayer({
        source: new OSM(),
      }),
    ],
    view: new View({
      center: iiscLocation,
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
