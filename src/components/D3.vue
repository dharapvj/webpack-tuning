<template>
  <div>
    <h1>d3 drawing demo</h1>
    <div class='d3root'></div>
  </div>
</template>

<script>
// improvement: import only what you need from D3
import { select } from 'd3-selection';
// import * as d3 from 'd3';

// d3.select('body').append('p');
const drawRect = () => {
  select('.d3root')
    .append('svg')
      .attr('width', 960)
      .attr('height', 400)
    .append('g')
      .attr('transform', 'translate(20,20)')
    .append('rect')
      .attr('width', 920)
      .attr('height', 360)
      .attr('fill', 'aquamarine');
};

export default {
  mounted() {
    drawRect();
  },
};
</script>
