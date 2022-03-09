<template>
  <div id="app">
    <VueHeader/>
    <VueMain/>
    <VueFooter/>
    <vueFooterSocial/>
  </div>
</template>

<script>
import VueHeader from './components/VueHeader.vue';
import VueMain from './components/VueMain.vue';
import VueFooter from './components/VueFooter.vue';
import VueFooterSocial from './components/VueFooterSocial.vue'


export default {
  name: 'App',
  components: {
    VueHeader,
    VueMain,
    VueFooter,
    VueFooterSocial,
  }
}
</script>

<style lang="scss">

@import url('https://fonts.googleapis.com/css2?family=League+Gothic&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'League Gothic', sans-serif;
  font-size:18px;
  font-weight: 300;
}
.container-fluid{
  width: 100%;
  min-height: 100px;
  margin: 0 auto;
}

.container{
  width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
}
li{
  list-style: none;
}
a{
  text-decoration: none;
  color: currentColor;
}
</style>
