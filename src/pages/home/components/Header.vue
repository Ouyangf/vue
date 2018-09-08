<template>
  <div class="header">
    <div class="header-left">
        <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
      {{this.city}}
        <span class="iconfont arrow-icon" >&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import '../../../assets/style/varibles.styl'
  .header
    display: flex
    color: #fff
    background: $bgColor
    .header-left
      width: 2.64rem
      padding-top: 12px
      float: left
      .back-icon
        text-align: center
        font-size: 1.4rem
    .header-input
      flex: 1
      height: 2.64rem
      line-height: 2.64rem
      margin-top: .12rem
      margin-left: -0.5rem
      padding-left: .2rem
      background: #fff
      border-radius: 1.1rem
      color: #ccc
    .header-right
      min-width: 3.04rem
      padding: 15px 0.1rem
      float: right
      text-align: center
      color: #fff
      .arrow-icon
        margin-left: -.04rem
        font-size: .24rem
</style>
