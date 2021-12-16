<template>
  <div class="wrapper-nav">
    <nav>
      <a href="/" class="logotip">
        <img src="@/assets/images/logotip.jpg" alt="">
      </a>
      <!-- <NuxtLink to="/" class="btn-search">Знакомства для успешных мужчин
      </NuxtLink> -->
    </nav>
    <div class="categories">
      <a href="#" class="active">Знакомства</a>
      <a href="#">Рейтинги</a>
      <a href="#">Отношения</a>
      <a href="#">Они и она</a>
      <a href="#">Советы</a>
      <a href="#">Всё о сексе</a>
      <a href="#">Фетиш</a>
      <a href="#">БДСМ</a>
      <a href="#">Интересное</a>
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
        content: 'Journal';
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
      background-color: #fe2c55;
      color:#fff;
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
  }
  .categories {
    display: block;
    margin:2px auto;
    width: 900px;
    height:44px;
    box-sizing:border-box;
    padding:0;
    border:1px;
    border-style:solid none none none;
    border-color:#ced8e7;
    text-align: center;
    text-transform: uppercase;
    a {
      display: inline-block;
      margin:0px 10px;
      box-sizing:border-box;
      padding:15px 0;
      color:#555;
      height:39px;
      font-family: Roboto Bold;
      font-size: 13px;
      text-decoration: none;
      transition: .3s;
      &.active {
        color:#111 !important;
      }
      &:hover {
        color:#fe2c55;
      }
    }
  }
}
</style>