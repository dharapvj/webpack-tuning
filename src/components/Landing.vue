<template src="./landing/template.html"></template>

<script>
/* import Moment from '@/components/Moment';
import Lodash from '@/components/Lodash';
import OpenLayers from '@/components/OpenLayers';
import D3 from '@/components/D3';*/

export default {
  data() {
    return {
      comp: 'bootstrap',
    };
  },
  methods: {
    route(where) {
      // console.log('clicked', where);
      this.comp = where;
    },
  },
  components: {
    /* Moment,
    Lodash,
    D3,
    OpenLayers, */
    // Improvement: Lazy load all the individual pages...
    // thereby reduce 1st page load bundle size dramatically!
    Moment: () => import('@/components/Moment'),
    Lodash: () => import('@/components/Lodash'),
    D3: () => import('@/components/D3'),
    OpenLayers: () => import('@/components/OpenLayers'),
  },
};
</script>

<!-- Improvement: load customized SCSS file for bootstrap, loading only what you need. -->
<style lang="scss" src="./landing/bootstrap-custom.scss"></style>
