<template>
  <div id="app">
    <VueHeader/>
    <VueMain/>
    <VueFooter/>
  </div>
</template>

<script>
import VueHeader from './components/VueHeader.vue';
import VueMain from './components/VueMain.vue';
import VueFooter from './components/VueFooter.vue';


export default {
  name: 'App',
  components: {
    VueHeader,
    VueMain,
    VueFooter
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
.container-fluid{
  width: 100%;
  min-height: 100px;
}

.container{
  width: 1200px;
  margin: 0 auto;
}
li{
  list-style: none;
}
a{
  text-decoration: none;
  color: currentColor;
}
</style>
