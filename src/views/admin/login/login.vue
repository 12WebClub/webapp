<template>
  <div class="login">
    <Atopbar>
      <div slot="left"></div>
      <div slot="right">
        <span class="iconfont icon-error"></span>
      </div>
    </Atopbar>
    <div class="l-body">
      <div class="form">
        <div class="f-item">
          <input type="text" v-model=value>
        </div>
        <div class="f-item">
          <input type="text" v-model=value>
        </div>
        <div class="f-item">
          <mt-button style="width: 100%" size="small" type="primary">登录</mt-button>
        </div>
        <div class="f-item help">
         <span>立即注册</span>
         <span>忘记密码？</span>
        </div>
      </div>
    </div>
    <div class="l-other-login">
      <h3>其他登录</h3>
      <div class="other">
        <div class="other-item">1</div>
        <div class="other-item">2</div>
        <div class="other-item">3</div>
      </div>
    </div>
  </div>
</template>

<script>
import Atopbar from './../../../components/A-topbar';

export default {
  components: {
    Atopbar,
  },
  data() {
    return {
      value: 123,
    };
  },
};
</script>

<style scoped lang="scss">
  @import './../../../assets/css/main';
  .login {
    position: relative;
    height: 100%;
    width: 100%;
    padding: 0.45rem 0 0 0;
    .l-body {
      padding: 0.9rem 0.15rem 0 0.15rem;
      .form {
        .f-item {
          width: 100%;
          height: 0.35rem;
          margin-bottom: 0.2rem;
        }
        .help {
          padding-top: 0.1rem;
          display: flex;
          justify-content: space-between;
          color: #242424;
        }
      }
    }
    .l-other-login {
      width: 100%;
      position: fixed;
      bottom: 0.3rem;
      h3 {
        font-size: 0.12rem;
        text-align: center;
        margin-bottom: 0.2rem;
        color: #bababa;
      }
      .other {
        display: flex;
        justify-content: space-around;
        .other-item {
          width: 0.4rem;
          height: 0.4rem;
          background: $main-color;
          border-radius: 50%;
          text-align: center;
          line-height: 0.4rem;
        }
      }
    }
  }
</style>
