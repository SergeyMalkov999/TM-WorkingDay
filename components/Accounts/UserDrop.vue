<template>
  <div class="userdrop">
    <div class="wrapper">
    </div>
    <div class="conteaner-userdrop-wrapper">
      <div class="conteaner-userdrop">
        <div class="header">
          <div class="conteaner-avatar">
            <img src="@/assets/images/ts/29.jpg" alt="">
          </div>
          <p class="name-and-age">Анастасия, 27 лет</p>
          <p class="city-country">Москва, Россия</p>
          <a href="#" class="btn-write-message">Написать сообщение</a>
          <a href="#" class="btn-more-options"></a>
          <!-- 
          Выше ссылка 3 точки, при клике на которую должно всплывать модальное меню с пунтами 
          --- Добавить в избранное
          --- Заблокировать пользователя
          --- Отмена
          -->
        </div>
        <div class="user-information">
          <p>Милая, молодая девушка в поисках настоящего мужчины. Живу в моменте, со мной не соскучишься 😉</p>
          <hr>
          <p><span>Внешность:</span> 175 см, 45 кг, Блондина с голубыми глазами, смешанной внегности, обычным телосложением. Водолей</p>
          <p><span>Цель знакомства:</span> Найти спонсора, путешествовать вместе, постоянные отношения</p>
        </div>
        <div class="gallery">
          <a href="@">
            <img src="@/assets/images/ts/2.jpg" alt="">
          </a>
          <a href="@">
            <img src="@/assets/images/ts/3.jpg" alt="">
          </a>
          <a href="@">
            <img src="@/assets/images/ts/4.jpg" alt="">
          </a>
          <a href="@">
            <img src="@/assets/images/ts/5.jpg" alt="">
          </a>
          <a href="@">
            <img src="@/assets/images/ts/6.jpg" alt="">
          </a>
          <a href="@">
            <img src="@/assets/images/ts/7.jpg" alt="">
          </a>
          <a href="@">
            <img src="@/assets/images/ts/8.jpg" alt="">
          </a>
          <a href="@">
            <img src="@/assets/images/ts/9.jpg" alt="">
          </a>
        </div>
        <a href="#" class="close"></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserDrop',
  components: {

  },
  data() {
    return {
      
    }
  },
  methods: {
    
  },
  computed: {

  }
}
</script>

<style scoped lang="scss">
.userdrop {
  .wrapper {
    display: block;
    position: fixed;
    top:0;
    left:0;
    right:0;
    bottom:0;
    width:100%;
    height:100%;
    background-color: rgba(0, 0, 0, 0.6);
    z-index: 999;
  }
  .conteaner-userdrop-wrapper {
    position: absolute;
    display: grid;
    width:600px;
    top:0;
    left: 50%;
    transform: translateX(-50%);
    z-index: 9999;
    padding:0;
    .conteaner-userdrop {
      position: relative;
      display: grid;
      grid-template-rows: min-content min-content min-content min-content;
      margin: 65px 0 20px;
      border-radius: 26px;
      background: #fff;
      padding: 10px;
      box-sizing:border-box;
      .header {
        position: relative;
        width:100%;
        height:content;
        margin:0 0 0 0;
        text-align: center;
        padding-top:45px;
        .conteaner-avatar {
          position: absolute;
          width:80px;
          height:80px;
          border-radius: 60px;
          overflow: hidden;
          border:5px solid #fff;
          left: 50%;
          transform: translateX(-50%);
          background: #fff;
          top:-50px;
          img {
            width:100%;
          }
        }
        .name-and-age {
          color:#111;
          font-family: Roboto Black;
          font-size: 19px;
        }
        .city-country {
          font-family: Roboto Medium;
          color:#313131;
          font-size: 15px;
        }
        .btn-write-message {
          width: 210px;
          display: inline-block;
          background: #fe2c55;
          border-radius: 24px;
          text-align: center;
          margin:14px 0 0 0;
          box-sizing: border-box;
          font-family: Roboto Regular;
          color:#fff;
          font-size: 14px;
          height:34px;
          padding:9px 0 0 0;
          text-decoration: none;
          transition: .3s;
        }
        .btn-more-options {
          display: block;
          position: absolute;
          width: 50px;
          background: #fff;
          border-radius: 24px;
          margin:14px 0 0 14px;
          box-sizing: border-box;
          height:36px;
          text-decoration: none;
          background-image: url(~@/assets/images/three-dots.svg);
          background-size: 21px;
          background-position: 15px 8px;
          background-repeat: no-repeat;
          transition: .3s;
          top:-15px;
          right:0;
        }
        .btn-write-message:hover, .btn-more-options:hover {
          filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
          -moz-opacity: 0.8;
          -khtml-opacity: 0.8;
          opacity: 0.8;
        }
      }
      .user-information {
        position: relative;
        width:530px;
        margin: 20px auto 0;
        background:#f5f2ed;
        border-radius: 16px;
        padding: 20px 20px 16px;
        box-sizing: border-box;
        p {
          color:#111;
          box-sizing: border-box;
          &:nth-child(1) {
            font-family: Roboto Medium;
            font-size: 15px;
            padding:0;
          }
          &:nth-child(3), &:nth-child(4) {
            font-family: Roboto Regular;
            color: #666 !important;
            font-size: 14px;
            padding:5px 0;
            span {
              color:#111;
              font-family: Roboto Medium;
            }
          }
        }
        hr {
          border:0;
          height:2px;
          background: #fff;
          width:100%;
          margin: 17px 0 12px;
          border-radius: 2px;
        }
      }
      .gallery {
        position: relative;
        width:530px;
        margin: 35px auto 20px;
        display: grid;
        grid-template-columns: auto auto auto;
        gap: 10px;
        a {
          display: block;
          height:240px;
          overflow: hidden;
          background: #fff;
          border-radius: 14px;
          img {
            width:100%;
            height: 100%;
            object-fit: cover;
            transition: .3s;
          }
          &:hover {
            img {
              filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
              -moz-opacity: 0.8;
              -khtml-opacity: 0.8;
              opacity: 0.8;
            }
          }
        }
      }
    }
  }
  .close {
    display: block;
    position: fixed;
    width: 36px;
    height: 36px;
    background: #fff;
    border-radius: 30px;
    top: 0;
    left: 50%;
    margin: 74px 0 0 320px;
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
</style>