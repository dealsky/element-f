<template>
  <div class="login">
    <el-form class="login-form">
      <h3 class="title">系统登录</h3>

      <el-form-item>
        <el-input type="text" placeholder="账号">
          <i class="icon icon-user" slot="prefix"></i>
        </el-input>
      </el-form-item>

      <el-form-item class="input-wrapper">
        <el-input class="input" type="password" placeholder="密码">
          <i class="icon icon-lock" slot="prefix"></i>
          <i class="icon-suffix icon-eye_off" slot="suffix"></i>
        </el-input>
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

<style lang="stylus">
  @import "../../common/stylus/icon.styl"
  @import "../../common/stylus/variables.styl"

  .login
    position: fixed
    width 100%
    height 100%
    background #303a49
    .login-form
      margin 120px auto 0 auto
      padding 35px 35px 15px 35px
      box-sizing border-box
      width 500px
      .title
        margin-bottom 40px
        text-align center
        font-size 26px
        color: #eee
      .el-form-item
        margin-bottom: 22px
        .el-input
          border: 1px solid $color-border-l
          border-radius 4px
          input
            background #2b3442
            border: 0
            color: #eee
          .icon
            display inline-block
            vertical-align top
            margin-top: 12px
            font-size: 16px
            color: #8b99a3
          .icon-suffix
            display: inline-block;
            margin-top: 10px;
            vertical-align: top;
            font-size 24px
            color: #8b99a3
      .btn-login
        width 100%
</style>
