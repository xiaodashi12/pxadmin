<template>
  <div>
    <div style="display: flex;flex-direction: row">
      <img src="@/assets/login_img.png" alt="" class="login-img">
      <div style="flex: 1;background-color: #fff;position: relative;">
          <div style="display: flex;flex-direction: column;justify-content: center;margin: 6.6rem 13.5rem 0 13.5rem"
                v-on:keyup.enter="loginReq">
            <div style="margin-left: 4.26rem">
                <!-- <div class="login-en-text">BDI-IoT</div> -->
                <div class="login-cn-text">矿车驾驶平台</div>
                <div class="login-text">欢迎您 ! 请登入您的账号</div>
            </div>
            <div class="login-id-container">
                <img src="@/assets/login_people.svg" alt="" class="login-id-icon">
                <input class="login-input" type="text" placeholder="请输入您的用户名" v-model="userName">
            </div>
            <div class="login-password-container">
                <img src="@/assets/login_password.svg" alt="" class="login-password-icon">
                <input class="login-input" type="password" placeholder="请输入您的密码" v-model="password">
            </div>
            <div style="display: flex;flex-direction: row;margin-top: 4.6rem;justify-content: center;">
                <button @click="loginReq" class="login-btn-lg">登入</button>
            </div>
            <div class="login-footer">
              淮北祥泰科技有限责任公司技术支持
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      //用户名
      userName: 'admin',
      //密码
      password: 'admin'
    }
  },
  methods: {
    //供给接口调用，判断是否登陆成功
    login(bool) {
     
      
    },
    //跳转到注册页面
    register() {
      this.$router.push('/LoginPage/Register')
    },
    //发起登录请求
    loginReq() {
    }
  },

}
</script>
</script>

<style scoped>
.login-footer {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: 32px;
    text-align: center;
    color: #143992;
}
.login-img{
  width:50vw ;
  height: 100vh;
  margin: -0.4rem 0 0 -0.6rem;
}
.login-en-text {
  font-size: 3.84rem;
  font-family: Source Sans Pro;
  font-weight: bold;
  letter-spacing: 1rem;
  color: #143992;
}

.login-cn-text {
  font-size: 2.16rem;
  font-weight: bold;
  letter-spacing: 0.46rem;
  color:#143992;
  text-align: center;
}

.login-text {
  font-weight: 400;
  font-size: 1.21rem;
  color: #A6A7AD;
  text-align: center;
  margin: 2.8rem 0 2.8rem 0rem;
}

.login-id-container {
  display: flex;
  flex-direction: row;
  border-bottom: 0.16rem solid #E9E9F0;
  margin-bottom: 2rem;
}

.login-id-icon {
  width: 1rem;
  height: 1rem;
  margin: 0.36rem 0.6rem 0.2rem 0.6rem
}

.login-password-container {
  display: flex;
  flex-direction: row;
  border-bottom: 0.16rem solid #E9E9F0
}

.login-password-icon {
  width: 2rem;
  height: 1.8rem;
  margin: 0.16rem 0.1rem 0rem 0.1rem;
}

.login-input {
  width: 26rem;
  height: 2rem;
  border: none;
  font-size: 1.08rem;
  color: #43425D;
  display: flex;
  flex-direction: row;
  align-items: center;
}

.login-btn-lg {
  width: 12.49rem;
  height: 3.37rem;
  background:#143992;
  color: white;
  border-radius: 1.6rem;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.21rem;
}

.login-btn-rg {
  border: 0.06rem solid #143992;
  border-radius: 1.6rem;
  width: 12.49rem;
  height: 3.37rem;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.21rem;
  color: #143992;
  margin-left: 3.66rem;
  background: white;
}
</style>