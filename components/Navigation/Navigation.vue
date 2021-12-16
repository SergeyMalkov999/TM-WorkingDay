<template>
  <div class="wrapper-nav">
    <nav>
      <a href="/" class="logotip">
        <img src="@/assets/images/logotip.jpg" alt="">
      </a>
      <NuxtLink to="/" class="btn-search">Я ищу мужчину
      </NuxtLink>

      <!-- Скрываем весь контейнер user-nav для не авторизованного пользователя. Принцип скрытия - меняем стиль на display:none; -->

      <div class="user-nav">
        <a href="#" class="link-avatar-drop" @mouseenter="mouseenter" @mouseleave="mouseleave">
          <div class="conteanr-avatar-drop">
            <!-- <img src="" alt=""> -->
          </div>
        </a>
         <a href="#" class="btn-navigation-ico natification">
          <!-- Счётчик количества сообщений/обновлений -->
          <!-- <span class="counter">1</span> -->
        </a>
        <a href="#" class="btn-navigation-ico guest">
          <!-- Счётчик количества сообщений/обновлений -->
          <!-- <span class="counter">2</span> -->
        </a>
        <NuxtLink to="/direct" class="btn-navigation-ico comments">
          <!-- Счётчик количества сообщений/обновлений -->
          <!-- <span class="counter">3</span> -->
        </NuxtLink>
        <a href="#" class="btn-navigation-ico my-drop">
        </a>
        <div class="menu-drop-user" @mouseenter="enter" @mouseleave="leave" v-if="ActiveMenuDrop === true">
          <div class="conteaner-user-info">
            <p class="name">Денис</p>
            <!-- <span class="status-no-active">Premium</span> -->
            <span class="status-active">Premium</span>
            <p class="coint-balance">Монет: 0</p>
          </div>
          <a class="link editing">Редактировать анкету</a>
          <a class="link servise">Сервисы и услуги</a>
          <a class="link money">Купить монеты</a>
          <a class="link setting">Настройки</a>
          <a class="link exit">Выход</a>
        </div>
      </div>

      <!-- // -->

    </nav>
    <div class="search-parameters">
      <a href="#" class="active">Фотопад</a>
      <a href="#">Анкеты</a>
      <a href="#">Случайные</a>
      <a class="link-option-list-home">Условия поиска <span class="counter">1</span></a>
    </div>
  </div>
</template>
    
<script>
export default {
  name: 'NavAuth',
  components: {
    
  },
  data() {
    return {
      ActiveMenuDrop: 0,
    }
  },
  methods: {
    mouseenter: function() {
      this.ActiveMenuDrop = true
      clearTimeout(timerId);
    },
    mouseleave: function() {
      timerId = setTimeout(() => {
        this.BlockOver = false
      }, 1000)
    },
  },
  computed: {

  },
  post: {
    
  }
}
</script>

<style lang="scss" scoped>
.wrapper-nav {
  width:950px;
  height:content;
  min-height:65px;
  margin:10px;
  z-index: 999;
  background: #f5f2ed;
  border-radius: 22px;
  nav {
    position: relative;
    width:900px;
    margin:0 auto;
    height:60px;
    box-sizing:border-box;
    .logotip {
      margin:19px 0 0 0;
      float:left;
      transition: .3s;
      text-decoration: none;
      &:hover {
        filter:progid:DXImageTransform.Microsoft.Alpha(opacity=70);
        -moz-opacity: 0.7;
        -khtml-opacity: 0.7;
        opacity: 0.7;
      }
      &::after {
        position: absolute;
        top:18px;
        left:170px;
        content: 'Dating';
        text-decoration: none;
        border:1px;
        border-style:none none none solid;
        border-color:#cccccc;
        height:30px;
        padding:8px 0 0 14px;
        box-sizing:border-box;
        font-family: Roboto Regular;
        font-size: 14px;
        color:#74749c;
      }
    }
    .link {
      float:left;
      font-family: Roboto Bold;
      font-size: 17px;
      color:#4d4d4d;
      text-decoration: none;
      transition: .3s;
      margin:21px 0 0 35px;
      cursor: pointer;
      &:hover {
        color:#111;
      }
    }
    .btn-search {
      display: block;
      position: absolute;
      height:34px;
      padding:9px 30px;
      box-sizing:border-box;
      font-family: Roboto Medium;
      font-size: 15px;
      left: 50% !important;
      transform: translateX(-50%) !important;
      top:0;
      margin:16px 0 0 0;
      text-decoration: none;
      transition: .3s;
      border-radius: 40px;
      line-height: 16px;
      width:auto;
      background-color: #fff;
      color:#4e4e81;
      cursor: pointer;
      text-align: center;
      box-shadow: 0px 7px 25px 0px rgba(34, 60, 80, 0.05);
      &:hover {
        filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
        -moz-opacity: 0.8;
        -khtml-opacity: 0.8;
        opacity: 0.8;
      }
    }
    .user-nav {
      position: relative;
      width:content;
      height:auto;
      float:right;
      .link-avatar-drop {
        position:absolute;
        width:36px;
        height:36px;
        right:0;
        top:0;
        margin:15px 0 0 0;
        .conteanr-avatar-drop {
          position: relative;
          width:36px;
          height:36px;
          overflow: hidden;
          border-radius: 30px;
          background-color: #d0d1d3;
          background-image: url(~@/assets/images/avatar-drop.svg);
          background-size: 30px;
          background-position: center 12px;
          background-repeat: no-repeat;
          transition: .3s;
          img {
            width:100%;
            height: 100%; 
            object-fit: cover;
          }
        }
      }
      .btn-navigation-ico {
        width: auto;
        min-width: 40px;
        height:46px;
        display: block;
        float:right;
        &.my-drop {
          margin:13px 7px 0 0;
          background-image: url(~@/assets/images/my-drop.svg);
          background-size: 22px;
          background-position: 0 10px;
          background-repeat: no-repeat;
          &__active {
            background-image: url(~@/assets/images/my-drop.svg) !important;
          }
        }
        &.comments {
          margin:13px 7px 0 0;
          background-image: url(~@/assets/images/direct.svg);
          background-size: 22px;
          background-position: 0 10px;
          background-repeat: no-repeat;
          &__active {
            background-image: url(~@/assets/images/comments-active.svg) !important;
          }
        }
        &.guest {
          margin:13px 5px 0 0;
          background-image: url(~@/assets/images/guest.svg);
          background-size: 22px;
          background-position: 0 9px;
          background-repeat: no-repeat;
          &__active {
            background-image: url(~@/assets/images/mailinglist-active.svg) !important;
          }
        }
        &.natification {
          margin:13px 40px 0 0;
          background-image: url(~@/assets/images/natification.svg);
          background-size: 22px;
          background-position: 0 9px;
          background-repeat: no-repeat;
          &__active {
            background-image: url(~@/assets/images/natification-active.svg) !important;
          }
        }
        .counter {
          float:left;
          margin:5px 0 0 13px;
          min-width: 20px;
          height: 20px;
          border-radius: 17px;
          background-color: #fe2c55;
          color: #fff;
          font-family: Roboto Bold;
          font-size: 12px;
          text-align: center;
          padding: 2px 4px 0 5px;
          box-sizing:border-box;
          border:1px solid #fff;
        }
        &:hover {
          filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
          -moz-opacity: 0.8;
          -khtml-opacity: 0.8;
          opacity: 0.8;
        }
      }
      .menu-drop-user {
        position:absolute;
        z-index: 999;
        right:-15px;
        top:58px;
        width:260px;
        height:auto;
        border-radius: 14px;
        background-color: #fff;
        box-shadow:0 0 30px 0 rgba(0, 0, 0, 0.15);
        padding:10px 0 0 0;
        &::before {
          content: '';
          position: absolute;
          margin:0;
          top:-8px;
          right:26px;
          width: 0; 
          height: 0;
          border-left: 8px solid transparent;
          border-right: 8px solid transparent;
          border-bottom: 8px solid #fff;
        }
        .conteaner-user-info {
          width:100%;
          height:76px;
          border:1px;
          border-color:#e7e7e7;
          border-style: none none solid none;
          margin:0 0 14px 0;
          padding: 12px 0 0 23px;
          box-sizing:border-box;
          color:#000;
          .name {
            font-family: Roboto Medium;
            font-size: 14px;
            margin:0 0 5px 0;
            float:left;
            width: 140px;
            overflow: hidden;
          }
          .status-active {
            position: relative;
            float:right;
            width:72px;
            height:17px;
            border-radius: 18px;
            font-size: 12px;
            background-color: #fe2c55;
            font-family: Roboto Medium;
            padding: 2px 0 0 0;
            box-sizing:border-box;
            color:#fff;
            text-align: center;
            text-transform: uppercase;
            margin:0 20px 0 0;
          }
          .status-no-active {
            position: relative;
            float:right;
            width:72px;
            height:17px;
            border-radius: 18px;
            font-size: 12px;
            background-color: #d2d2d2;
            font-family: Roboto Medium;
            padding: 2px 0 0 0;
            box-sizing:border-box;
            color:#fff;
            text-align: center;
            text-transform: uppercase;
            margin:0 20px 0 0;
            &::before {
              content: '';
              position: absolute;
              top:8px;
              left:0;
              width:72px;
              height:1px;
              background-color: #fff;
            }
          }
          .coint-balance {
            font-family: Roboto Medium;
            font-size: 14px;
            margin:7px 0 5px 0;
            color:#4d4d4d;
            float:left;
            width: 140px;
            overflow: hidden;
          }
        }
        .link {
          display: block;
          position: relative;
          width:100%;
          height:40px;
          margin:0 0 0 0;
          padding:10px 0 0 60px;
          box-sizing:border-box;
          color:#161823;
          font-family: Roboto Bold;
          font-size: 16px;
          background-color: #fff;
          transition: .3s;
          text-decoration: none;
          &:hover {
            background-color: #f8f8f8;
            color:#111;
          }
          &.editing {
            background-image: url(~@/assets/images/ico-menu-user/editing.svg);
            background-size: 20px;
            background-position: 20px 10px;
            background-repeat: no-repeat;
          }
          &.addphoto {
            background-image: url(~@/assets/images/ico-menu-user/addphoto.svg);
            background-size: 20px;
            background-position: 18px 10px;
            background-repeat: no-repeat;
          }
          &.servise {
            background-image: url(~@/assets/images/ico-menu-user/servise.svg);
            background-size: 20px;
            background-position: 18px 10px;
            background-repeat: no-repeat;
          }
          &.money {
            background-image: url(~@/assets/images/ico-menu-user/money.svg);
            background-size: 20px;
            background-position: 18px 12px;
            background-repeat: no-repeat;
          }
          &.setting {
            background-image: url(~@/assets/images/ico-menu-user/setting.svg);
            background-size: 19px;
            background-position: 19px 10px;
            background-repeat: no-repeat;
          }
          &.exit {
            color:#9d9d9d;
            border:1px;
            border-color:#e7e7e7;
            border-style: solid none none none;
            margin-top:10px !important;
            height: 60px !important;
            padding:20px 20px;
            border-radius: 0 0 14px 14px;
            &:hover {
              color:#161823;
            }
          }
        }
      }
    }
  }
  .search-parameters {
    display: block;
    margin:2px auto;
    width: 900px;
    height:44px;
    box-sizing:border-box;
    padding:0;
    border:1px;
    border-style:solid none none none;
    border-color:#ced8e7;
    a {
      float:left;
      margin:0px 30px 0 0;
      box-sizing:border-box;
      padding:13px 0;
      color:#4e4e81;
      height:39px;
      font-family: Roboto Medium;
      font-size: 15px;
      text-decoration: none;
      transition: .3s;
      &.active {
        color:#111 !important;
      }
      &:hover {
        color:#fe2c55;
      }
    }
    .link-option-list-home {
      float:right;
      margin:6px 0 0 0;
      box-sizing:border-box;
      background-color: #ced8e7;
      padding:7px 20px 0 46px;
      border-radius:14px;
      color:#4e4e81;
      height:31px;
      font-family: Roboto Medium;
      font-size: 15px;
      text-decoration: none;
      transition: .3s;
      background-image: url(~@/assets/images/settings-list.svg);
      background-size: 16px;
      background-repeat: no-repeat;
      background-position: 15px 8px;
      cursor: pointer;
      .counter {
        padding:2px 6px;
        background:#fe2c55;
        color:#fff;
        border-radius: 20px;
        margin:0 0 0 6px;
        font-family: Roboto Regular;
        font-size: 13px;
      }
      &:hover {
        color:#fe2c55;
      }
    }
    .btn-drawing-conditions {
      position: relative;
      float:right;
      width:95px;
      height:31px;
      background-color: #ced8e7;
      border-radius: 14px;
      margin:6px 5px 0 0;
      overflow: hidden;
      padding:3px;
      box-sizing:border-box;
      cursor: pointer;
      transition: .3s;
      .switch {
        float:left;
        margin:0 0 0 0;
        width:45px;
        height:25px;
        background-color: #fff;
        border-radius: 14px;
        transition: .3s;
        &.right {
          margin:0 0 0 44px;
        }
      }
      .switch-left-ico {
        top:10px;
        left:16px;
        position: absolute;
        z-index:1;
        width:20px;
        height:20px;
        background-image: url(~@/assets/images/ico-switch-left.png);
        background-size: 20px;
        background-position: 0 0;
        background-repeat: no-repeat;
        transition: .3s;
      }
      .switch-right-ico {
        top:8px;
        left:62px;
        position: absolute;
        z-index:1;
        width:18px;
        height:17px;
        background-image: url(~@/assets/images/ico-switch-right.png);
        background-size: 18px;
        background-position: 0 0;
        background-repeat: no-repeat;
        transition: .3s;
      }
      .activeleft {
        filter:progid:DXImageTransform.Microsoft.Alpha(opacity=55);
        -moz-opacity: 0.55;
        -khtml-opacity: 0.55;
        opacity: 0.55;
      }
      .activeright {
        filter:progid:DXImageTransform.Microsoft.Alpha(opacity=55);
        -moz-opacity: 0.55;
        -khtml-opacity: 0.55;
        opacity: 0.55;
      }
    }
  }
}
</style>