<template>
  <div class="login">
    <el-form class="login-form">
      <h3 class="title">系统登录</h3>
      <div class="input-wrapper">
        <span class="icon-user"></span>
        <el-input class="input"></el-input>
      </div>
      <div class="input-wrapper">
        <i class="icon-lock"></i>
        <el-input class="input"></el-input>
      </div>
      <el-button class="btn-login" type="primary">登录</el-button>
    </el-form>
  </div>
</template>

<script>
export default {
  name: "login"
};
</script>

<style lang="stylus" scoped>
  @import "../../common/stylus/icon.styl"
  @import "../../common/stylus/variables.styl"

  .login
    .login-form
      margin 200px auto 0 auto
      padding 35px 35px 15px 35px
      box-sizing border-box
      width 520px
      .title
        margin-bottom 40px
        text-align center
        font-size 26px
      .input-wrapper
        margin-bottom: 22px
        .icon-user
          display: inline-block
        .input
          width 85%
      .btn-login
        width 100%
</style>
