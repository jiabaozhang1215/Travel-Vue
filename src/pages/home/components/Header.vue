<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩/主题
    </div>
    <router-link to="/city">
      <div class="header-right">
      {{this.city}}
      <span class="iconfont arrow-icon">&#xe6aa;</span>
    </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from "vuex"

export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city']) // 将vuex中state存储的city映射到当前组件的计算属性city上
  }
}
</script>

<!-- 使用stylus -->
<!-- 1rem = (html的font-size) = 50px -->
<style lang="stylus" scoped>
@import '~styles/varibles.styl'

  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      text-align: center
      margin-left: .12rem
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      background: #fff
      margin-top: .12rem
      padding-left: .2rem
      line-height: .64rem
      height: .64rem
      margin-left: .2rem
      border-radius: .1rem
      color: #ccc
    .header-right
      float: right
      margin: 0 .15rem
      text-align: center
      color: #fff
      .arrow-icon
        font-size: .35rem
        margin-left: -.05rem
</style>
