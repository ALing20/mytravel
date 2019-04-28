<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xeb99;</span>
    </div>
    <div class="header-input">
      <span class="iconfont iconicon_search"></span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市<span class="iconfont iconsort-down arrow-icon"></span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style scoped lang="less">
// 引入全局样式
// 1. 相对路径
  // @import '../assets/styles/varibles.less';
  // 2. 使用波浪线
  @import '~@/assets/styles/varibles.less';
  // 3. 在配置文件里配置styles路径为src/assets/styles
  // npm install --save style/border.css style/iconfont.css style/reset.css
  // @import '~style/varibles.less';
  // 86px 二倍图 则应该给43px
  // 1rem = html font-size = 50px
  // 86/100 rem
  .header {
    display: flex;
    height: .86rem;
    line-height: .86rem;
    background-color: @bgcolor;
    color: #fff;
    .header-left {
      width: .64rem;
      float: left;
      text-align: center;
      .back-icon {
        font-size: .4rem;
      }
    }
    .header-input {
      flex: 1;
      margin: .12rem .2rem;
      padding-left: .2rem;
      line-height: .62rem;
      background-color: #fff;
      border-radius: .1rem;
      color: #ccc;
    }
    .header-right {
      width: 1.24rem;
      float:right;
      .arrow-icon {
        font-size: .24rem;
      }
    }
  }
</style>
