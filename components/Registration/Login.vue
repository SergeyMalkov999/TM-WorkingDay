<template>
  <div class="registration">
    <div class="wrapper"></div>
    <div class="conteaner-registration">
      <p class="logotip"><img src="@/assets/images/logotip-white.jpg" alt=""></p>
      <p class="salute">Войдите, чтобы общаться</p>
      <p class="additional-salute">Используйте почту и пароль для входа. Или воспользуйтесь социальными сетями</p>
      <form class="fast-registration">
        <input type="text" name="" id="" class="fast-inp" placeholder="E-Mail указанный при регистрации">
        <input type="password" name="" id="" class="fast-inp" placeholder="Ваш пароль">
        <a href="#" class="fast-btn">Войти</a>
      </form> 
      <a href="#" class="link-login"><span class="span">Ещё не зарегистрироаны? - </span>Зарегистрируйтесь</a>
      <a href="#" class="close"></a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Greating',
  components: {

  },
  data() {
    return {
    
    }
  },
  methods: {
   
  }
}
</script>

<style scoped lang="scss">
.registration {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 999999;
  top:0;
  transition: all 2s ease-in-out;
  -webkit-transition: all 2s ease-in-out;
  -moz-transition: all 2s ease-in-out;
  -o-transition: all 2s ease-in-out;
  .wrapper {
    display: block;
    position: fixed;
    top:0;
    left:0;
    right:0;
    bottom:0;
    width:100%;
    height:100%;
    background-color: rgba(0, 0, 0, 0.5);
  }
  .conteaner-registration {
    position: absolute;
    width:470px;
    height:auto;
    left:50%;
    top:13%;
    padding:50px 0 0;
    margin:0 0 0 -235px;
    background-color: #fff;
    border-radius: 22px;
    overflow: hidden;
    .logotip {
      width:100%;
      text-align: center;
      margin:0 0 30px;
    }
    .salute {
      width:360px;
      height:auto;
      margin:0 auto;
      text-align: center;
      font-family: Roboto Bold;
      font-size: 21px;
      color:#313131;
    }
    .additional-salute {
      width:360px;
      font-family: Roboto Light;
      margin:5px auto;
      font-size: 14px;
      font-weight: bold;
      line-height: 21px;
      text-align: center;
    }
    .fast-registration {
      width:100%;
      text-align: center;
      margin-top:23px;
      :nth-child(4) {
        position: relative;
        display: block;
        width:100%;
        color:#313131;
        font-family: Roboto Regular;
        margin:20px 0;
      }
      .btn-variates {
        text-decoration: none;
        display: block;
        position: relative;
        margin:8px auto;
        width:260px;
        height:40px;
        border:1px solid #e3e3e4;
        font-family: Roboto Medium;
        font-size: 14px;
        border-radius: 6px;
        color:#111;
        box-sizing:border-box;
        &:hover {
          border:1px solid #111;
        }
        &.fb {
          background-color: #4268b4;
          border:1px solid #4268b4 !important;
          color:#fff;
          padding:11px 0 0 0;
          background-image: url(~@/assets/images/facebook.svg);
          background-size: 22px;
          background-position: 22px 9px;
          background-repeat: no-repeat;
          padding:11px 0 0 27px;
        }
        &.vk {
          background-image: url(~@/assets/images/vk.svg);
          background-size: 23px;
          background-position: 22px 9px;
          background-repeat: no-repeat;
          padding:11px 0 0 27px;
        }
        &.instagram {
          background-image: url(~@/assets/images/instagram.svg);
          background-size: 22px;
          background-position: 23px 9px;
          background-repeat: no-repeat;
          padding:11px 0 0 27px;
        }
      }
      .fast-inp {
        width:260px;
        height:40px;
        border-radius: 6px;
        border:2px solid #c9c9c9;
        background-color: #fff;
        outline:none;
        box-sizing:border-box;
        padding:0 14px;
        font-size: 14px;
        margin:14px 0 0 0;
        font-family: Roboto Medium;
        transition: .3s;
        &:focus, &:hover {
          border:2px solid #111;
        }
        &::placeholder {
          color:#777;
        }
      }
      .fast-btn {
        display: block;
        position: relative;
        text-decoration: none;
        width:260px;
        height:40px;
        border-radius: 36px;
        border:2px solid #fe2c55;
        background-color: #fe2c55;
        outline:none;
        box-sizing:border-box;
        padding:10px 0;
        font-size: 15px;
        font-family: Roboto Medium;
        margin:14px auto;
        color:#fff;
        transition: .3s;
        &:hover {
        filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
        -moz-opacity: 0.8;
        -khtml-opacity: 0.8;
        opacity: 0.8;
      }
      }
    }
    .link-login {
      display: block;
      position: relative;
      text-decoration: none;
      width:100%;
      height:60px;
      background-color: #efefef;
      color:#fe2c55;
      transition: .3s;
      font-size: 15px;
      font-family: Roboto Medium;
      padding:22px 0 0 0;
      box-sizing:border-box;
      text-align: center;
      margin:60px 0 0 0;
      span {
        color:#111 !important;
      }
      &:hover {
        filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
        -moz-opacity: 0.8;
        -khtml-opacity: 0.8;
        opacity: 0.8;
      }
    }
    .close {
      display: block;
      position: fixed;
      width: 36px;
      height: 36px;
      background: #fff;
      border-radius: 30px;
      top: 13%;
      left: 50%;
      margin: 0 0 0 253px;
      background-image: url(~@/assets/images/close.svg);
      background-size: 15px;
      background-position: center center;
      background-repeat: no-repeat;
      transition: .3s;
      z-index: 9999;
      &:hover {
        filter:progid:DXImageTransform.Microsoft.Alpha(opacity=50);
        -moz-opacity: 0.5;
        -khtml-opacity: 0.5;
        opacity: 0.5;
      }
    }
  }
}
</style>