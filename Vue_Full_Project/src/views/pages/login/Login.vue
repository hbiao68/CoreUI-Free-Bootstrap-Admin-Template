<template>
  <div class="pages-login">
    <!--图片背景-->
    <div class="pages-login-bg"></div>

    <!-- 登录tab集合 -->
    <div class="pages-login-tab">
      <Tabs>
        <Tab-pane label="账号登录" icon="social-windows">
          <form action="#">
            <div class="row form-group">
              <div class="col-md-12">
                <label for="username">Username or Email</label>
                <input type="text" class="form-control">
              </div>
            </div>
            <div class="row form-group">
              <div class="col-md-12">
                <label for="password">Password</label>
                <input type="password" class="form-control">
              </div>
            </div>

            <div class="row form-group">
              <div class="col-md-12">
                <input type="submit" class="btn btn-primary" @click="loginAction" value="Login">
              </div>
            </div>
          </form>
        </Tab-pane>
        <Tab-pane label="微信扫码登录" icon="social-apple" class="text-center">
          <img src="../../../../static/img/ewm_.png">
        </Tab-pane>
        <Tab-pane label="忘记密码" icon="social-windows">
          <form action="#">
            <div class="row form-group">
              <div class="col-md-12">
                <label for="username">Username or Email</label>
                <input type="text" class="form-control" id="username">
              </div>
            </div>
            <div class="row form-group">
              <div class="col-md-12">
                <label for="password">Password</label>
                <input type="password" class="form-control" id="password">
              </div>
            </div>
            <div class="row form-group">
              <div class="col-md-12">
                <label for="password2">Repeat Password</label>
                <input type="password" class="form-control" id="password2">
              </div>
            </div>

            <div class="row form-group">
              <div class="col-md-12">
                <input type="submit" class="btn btn-primary" value="Sign up">
              </div>
            </div>
          </form>
        </Tab-pane>
      </Tabs>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  methods: {
    loginAction: function () {
      this.$router.push({name: 'Dashboard'})
    }
  }
}
</script>

<style scoped lang="scss">
  .pages-login{
    .pages-login-bg{
      position: fixed;
      top:0;
      left: 0;
      right: 0;
      bottom: 0;
      background-color: rgb(64, 64, 64);
      background-image: url(../../../../static/img/login_bg.jpg);
      background-position: center 0;
      background-repeat: no-repeat;
      background-size: cover;
      -webkit-background-size: cover;
    }

    .pages-login-tab{
      width: 400px;
      margin: 0 auto;
      position: relative;
      top: 250px;
    }
  }
</style>
