<template>
  <div class="login">
    <div class="login-form">
      <div class="input-wrapper">
        <el-input></el-input>
      </div>
      <div class="input-wrapper">
        <el-input></el-input>
      </div>

      <button class="submit">提交</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "login"
};
</script>

<style lang="stylus" scoped>
  .login
    .login-form
      margin: 25% auto 0 auto
      .input-wrapper
        width
</style>
