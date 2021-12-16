<template>
  <div class="greating">
    <p><img src="@/assets/images/drop.svg" alt=""></p>
    <p>Самые молочные знакомства</p>
    <p>Мы знаем как создать уникальный сервис премиум знакосмвт, для соединения людей. Без ботов, феков и других людей которые не настроены на формат общения. Начни прямо сейчас, регистрация бесплатна, и займёт 30 секунд.</p>
    <p><a>Присоедениться</a></p>
    <p>Это бесплатно</p>
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
.greating {
  display: grid;
  position: relative;
  width:950px;
  text-align: center;
  margin:0 auto;
  border-radius: 22px;
  padding: 0 0 0 0;
  :nth-child(1) {
    width:50px;
    margin:20px auto 10px;
    filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
    -moz-opacity: 0.8;
    -khtml-opacity: 0.8;
    opacity: 0.8;
  }
  :nth-child(2) {
    width:100%;
    margin:0;
    font-family: Roboto Light;
    // font-family: 'Source Serif Pro', serif;
    font-size: 46px;
    line-height: 48px;
  }
  :nth-child(3) {
    width:680px;
    font-family: Roboto Light;
    margin:5px auto 0;
    font-size: 14px;
    padding:0 35px;
    box-sizing:border-box;
    font-weight: bold;
    line-height: 21px;
  }
  :nth-child(4) {
    width:100%;
    margin:15px 0 0;
    padding: 0;
    a {
      display: inline-block;
      height:39px;
      line-height: 16px;
      padding-top:12px;
      box-sizing:border-box;
      font-family: Roboto Medium;
      font-size: 16px;
      text-decoration: none;
      transition: .3s;
      border-radius: 40px;
      width:190px;
      background-color: #ee5355;
      color:#fff;
      filter:progid:DXImageTransform.Microsoft.Alpha(opacity=100);
      -moz-opacity: 1;
      -khtml-opacity: 1;
      opacity: 1;
      cursor: pointer;
      &:hover {
        filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
        -moz-opacity: 0.8;
        -khtml-opacity: 0.8;
        opacity: 0.8;
      }
    }
  }
  :nth-child(5) {
    display: block;
    position: relative;
    width:100%;
    margin:0;
    color:#9f9f9f;
    text-align: center;
    font-family: Roboto Regular;
    font-size: 12px;
    margin:0 0 30px 0;
  }
}
</style>