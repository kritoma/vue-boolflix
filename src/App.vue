<template>
  <div id="app">
    <BaseHeader/>
    <BaseMain/>
  </div>
</template>

<script>
import BaseHeader from './components/block/BaseHeader.vue';
import BaseMain from './components/block/BaseMain.vue';


export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseMain

  }
}
</script>

<style lang="scss">
@import "./assets/style/global.scss";
</style>
