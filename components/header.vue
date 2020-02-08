<template>
  <div class="header-wrapper">
    <el-row class="header" type="flex" justify="space-between">
      <div class="logo">
        <img src="/logo.jpg" alt />
      </div>
      <!-- 菜单 -->
      <el-row class="navs" type="flex">
        <nuxt-link to="/">首页</nuxt-link>
        <nuxt-link to="/post">旅游攻略</nuxt-link>
        <nuxt-link to="/hotel">酒店</nuxt-link>
        <nuxt-link to="/air">国内机票</nuxt-link>
      </el-row>
      <!-- 登录/注册 -->
      <div>
        <nuxt-link to="user/logo">登录/注册</nuxt-link>
      </div>
    </el-row>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="less" scoped>
.header-wrapper {
  height: 60px;
  background: #fff;
  box-shadow: 0 3px 2px #ccceee
}
.header {
  width: 1000px;
  margin: 0 auto;
  .logo {
    width: 165px;
    padding-top: 10px;
    img {
      width: 100%;
      display: block;
    }
  }
  .navs {
    flex: 1;
    margin: 0 20px;
  }
    a {
      display: block;
      height: 60px;
      box-sizing: border-box;
      padding: 0 20px;
      margin: 0 20px;
      line-height: 60px;
      &:hover,
      &:focus,
      &:active {
        border-bottom: 5px #409eff solid;
        color: #409eff;
      }
    } 
    /deep/ .nuxt-link-exact-active {
      background: #409eff;
      color: #fff !important;
     
  }
}

</style>