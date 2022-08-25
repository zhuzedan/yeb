<template>
  <div>
    <el-form ref="form" :model="loginForm" class="loginContainer">
      <h3 class="loginTitle">登录系统</h3>
      <el-form-item>
        <el-input type="text" v-model="loginForm.username" placeholder="请输入用户名"></el-input>
      </el-form-item>
      <el-form-item>
        <el-input type="password" v-model="loginForm.password" placeholder="请输入密码"></el-input>
      </el-form-item>
      <el-form-item>
        <el-input type="text" v-model="loginForm.code" placeholder="点击图片更换验证码"></el-input>
        <img :src="captchaUrl">
      </el-form-item>
      <el-checkbox v-model="checked">记住我</el-checkbox>
      <el-button type="primary" style="width: 100%">登录</el-button>
    </el-form>
  </div>
</template>

<script>
export default {
  name: "Login",
  data() {
    return {
      captchaUrl: '',
      loginForm: {
        username: 'admin',
        password: '123'
      }
    }
  }
}
</script>

<style scoped>
  .loginContainer {
    border-radius: 15px;
    background-clip: padding-box;
    margin: 180px auto;
    width: 350px;
  }
  .loginTitle {
    margin: 0 auto;
  }
</style>