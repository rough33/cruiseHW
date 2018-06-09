<template>
  <div id="app">
    <m-header></m-header>
    <cruisehw></cruisehw>
    <c-footer></c-footer>
  </div>
</template>

<script type="text/ecmascript-6">
import cruisehw from './components/cruisehw'
import CFooter from './components/c-footer'
import MHeader from './components/m-header'
export default {
  components: {
    cruisehw,
    CFooter,
    MHeader
  }
}
</script>

<style scoped>
  #app {}
</style>
