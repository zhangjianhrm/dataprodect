<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
  import Home from './components/Home.vue'
export default {
  components: {
    'Home-app':Home
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">

</style>
