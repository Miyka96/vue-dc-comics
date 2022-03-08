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
}
</style>
