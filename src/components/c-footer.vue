<template>
  <div class="c-footer">
    <h1 class="text"></h1>
  </div>
</template>

<script type="text/javascript">
export default {}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  // @import "~common/stylus/variable"
  // @import "~common/stylus/mixin"

  .c-footer
    position: fixed
    left: 0
    bottom: 0
    z-index: 50
    width: 100%
    height: 20px
    text-align: center
    background-color: #fff
    box-shadow: 0 -1px 1px rgba(0, 0, 0, .1)
    .text
      display: inline-block
      vertical-align: top
      line-height: 20px
      font-size: 10px
</style>
