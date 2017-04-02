<template src="./landing/template.html"></template>

<script>
import Moment from '@/components/Moment';
import Lodash from '@/components/Lodash';
import OpenLayers from '@/components/OpenLayers';
import D3 from '@/components/D3';

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
    Moment,
    Lodash,
    D3,
    OpenLayers,
  },
};
</script>

<style src="bootstrap/dist/css/bootstrap.min.css"></style>
