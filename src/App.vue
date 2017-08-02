<template>
  <div id="app">
    <m-header></m-header>
    <tab></tab>
    <keep-alive>
      <router-view></router-view>
    </keep-alive>
    <player></player>
  </div>
</template>

<script>
import MHeader from 'components/m-header/m-header'
import Tab from 'components/tab/tab'
import Player from 'components/player/player'

export default {
  name: 'app',
  components: {
    MHeader,
    Tab,
    Player
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
@import "~common/stylus/variable"

.tab
  display: flex;
  height: 44px;
  line-height: 44px;
  font-size: $font-size-medium;
  .tab-item
    flex: 1;
    text-align: center;
    .tab-link
      padding-bottom: 5px;
      color: $color-text-l;
    &.router-link-active
      .tab-link
        color: $color-theme;
        border-bottom: 2px solid $color-theme;
</style>
