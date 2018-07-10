<template>
  <div class="login">
    <el-form class="login-form">
      <h3 class="title">系统登录</h3>
      <el-form-item class="input-wrapper">
        <i class="icon icon-user"></i>
        <el-input class="input" type="text" placeholder="账号"></el-input>
      </el-form-item>

      <el-form-item class="input-wrapper">
        <i class="icon icon-lock"></i>
        <el-input class="input" type="password" placeholder="密码"></el-input>
      </el-form-item>
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
      .input-wrapper
        .icon
          display inline-block
        .input
          width 85%
      .title
        margin-bottom 40px
        text-align center
        font-size 26px
      .btn-login
        width 100%
</style>
