<template>
  <div>
    <div id="map" class="map"></div>
    <div>
      Usage of bootstrap
      <button type="button" class="btn btn-info">Info</button>
    </div>
  </div>
</template>

<script>
// Most stupidest way to import everything in one component
import _ from 'lodash';
import moment from 'moment';
import * as d3 from 'd3';
import ol from 'openlayers';

console.log(_.pick({
  RAM: '8gb',
  retina: true,
  screen: 'touch',
  lightning: true,
}, ['RAM', 'screen']));

moment().format('MMM Do YY');
d3.select('body').append('p');

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
      center: ol.proj.fromLonLat([37.41, 8.82]),
      zoom: 4,
    }),
  });
};

export default {
  data() {
    return {
    };
  },
  mounted() {
    drawMap();
  },
};
</script>

<style src="bootstrap/dist/css/bootstrap.min.css"></style>
<style src="openlayers/dist/ol.css"></style>
<style>
.map {
  height: 400px;
  width: 100%;
}
</style>
