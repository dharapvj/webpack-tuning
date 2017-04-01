<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
};
</script>

<style>
html {
    font-size: 62.5%;
}
body {
    font-size: 1.6rem;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 2.0rem;
    /*background-image: linear-gradient(to bottom, #f9f9ff 0%,#cbebff 69%,#a1dbff 100%)*/
}

p{
    font-size: 1.4rem;
}

</style>
