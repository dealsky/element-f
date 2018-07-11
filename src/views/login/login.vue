<template>
  <div class="login">
    <el-form :model="loginForm" :rules="loginRules" ref="loginForm" class="login-form">
      <h3 class="title">系统登录</h3>

      <el-form-item prop="username">
        <el-input type="text" placeholder="账号" v-model="loginForm.username">
          <i class="icon icon-user" slot="prefix"></i>
        </el-input>
      </el-form-item>

      <el-form-item prop="password">
        <el-input class="input" :type="passwd" placeholder="密码" v-model="loginForm.password">
          <i class="icon icon-lock" slot="prefix"></i>
          <i class="icon-suffix" :class="{ 'icon-eye_off': eyeOff, 'icon-eye': !eyeOff }" slot="suffix"
             @click="clickEye"></i>
        </el-input>
      </el-form-item>

      <el-button class="btn-login" type="primary" @click="handleLogin">登录</el-button>
    </el-form>
  </div>
</template>

<script>
export default {
  name: "login",
  data() {
    const validateUsername = (rule, value, callback) => {
      if (value === "") {
        callback(new Error("请输入账号"));
      } else {
        callback();
      }
    };

    const validatePassword = (rule, value, callback) => {
      if (value === "") {
        callback(new Error("请输入密码"));
      } else if (value.length < 6) {
        callback(new Error("密码长度不能小于6位"));
      } else {
        callback();
      }
    };

    return {
      eyeOff: true,
      loginForm: {
        username: "",
        password: ""
      },
      loginRules: {
        username: [{ validator: validateUsername, trigger: "blur" }],
        password: [{ validator: validatePassword, trigger: "blur" }]
      }
    };
  },
  computed: {
    passwd() {
      return this.eyeOff ? "password" : "text";
    }
  },
  methods: {
    clickEye() {
      this.eyeOff = !this.eyeOff;
    },
    handleLogin() {
      this.$refs.loginForm.validate(valid => {});
    }
  }
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
            font-size 20px
            color: #8b99a3
      .btn-login
        width 100%
</style>
