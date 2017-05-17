<template src="./landing/template.html"></template>

<script>
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
