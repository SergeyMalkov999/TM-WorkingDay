<template>
  <div>
    <!-- <div class="conteaner-header">
      <p>Фотопад девушек</p>
      <p>Бесконечный фотопад девушек. Листайте. Выбирайте. Пишите.</p>
    </div> -->
    <div class="list-drop">
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/1.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Кристина, 24</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/2.jpg" alt="">
        <span class="status active"></span>
        <span class="name-age">Анжелла, 32</span>
        <!-- <span class="active-top">PREMIUM</span> - выделение анкеты (платная услуга.). -->
      </a>
      <a href="#" class="conteaner-drop-prew ">
        <img src="@/assets/images/ts/3.jpg" alt="">
        <span class="status active"></span>
        <span class="name-age">Vutoria, 18</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/4.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Катя, 19</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/5.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Анжелла, 32</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/6.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Vutoria, 18</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/7.jpg" alt="">
        <span class="status active"></span>
        <span class="name-age">Катя, 19</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/8.jpg" alt="">
        <span class="status active"></span>
        <span class="name-age">Анжелла, 32</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/9.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Vutoria, 18</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/10.jpg" alt="">
        <span class="status active"></span>
        <span class="name-age">Дарья, 25</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/11.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Женя, 27</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/12.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Анжелла, 32</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/13.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Анжелла, 32</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/14.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Анжелла, 32</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/15.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Анжелла, 32</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/16.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Анжелла, 32</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/17.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Vutoria, 18</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/18.jpg" alt="">
        <span class="status active"></span>
        <span class="name-age">Катя, 19</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/19.jpg" alt="">
        <span class="status active"></span>
        <span class="name-age">Анжелла, 32</span>
      </a>
      <a href="#" class="conteaner-drop-prew">
        <img src="@/assets/images/ts/20.jpg" alt="">
        <span class="status noactive"></span>
        <span class="name-age">Vutoria, 18</span>
      </a>
    </div>
  </div>
</template>


<script>
export default {
  name: 'ListDrop',
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
.conteaner-header {
  position: relative;
  width:900px;
  height:content;
  margin:30px auto 40px;
  :nth-child(1) {
    width:100%;
    margin:0;
    font-family: Roboto Bold;
    font-size: 27px;
    line-height: 38px;
  }
  :nth-child(2) {
    width:900px;
    font-family: Roboto Light;
    margin:0 auto 0;
    font-size: 14px;
    padding:0 0;
    box-sizing:border-box;
    font-weight: bold;
    line-height: 21px;
  }
}
.list-drop {
  width:900px;
  height:auto;
  margin:30px auto;
  overflow: hidden;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  gap:14px;
  .conteaner-drop-prew {
    position: relative;
    height:270px;
    margin:0 0 0 0;
    border-radius: 14px;
    overflow: hidden;
    text-align: left;
    padding:0;
    vertical-align: top;
    transition: .3s;
    overflow: hidden;
    background: #fff;
    img {
      display: block;
      position: relative;
      width:100%;
      height: 100%;
      object-fit: cover;
      &.selected-drop {
        border:2px solid #fe2c55;
      	box-sizing:border-box;
      }
    }
    .status {
      position: absolute;
      z-index: 9;
      display: block;
      top:0;
      right:0;
      border-radius: 10px;
      margin:9px 9px 0 0;
      width:12px;
      height:12px;
      border:1px solid #fff;
      &.active {
        background-color:#67bc0f;
      }
      &.noactive {
        background-color:#b8b7b7;
      }
    }
    .name-age {
      position: absolute;
      z-index: 9;
      display: block;
      top:10px;
      left:12px;
      color:#fff;
      font-family: Roboto Medium;
      font-size: 11px;
    }
    .active-top {
      position: absolute;
      z-index: 9;
      display: block;
      bottom:10px;
      left:20px;
      width:130px;
      height:14px;
      text-align: center;
      border-radius: 30px;
      background: #ff5455;
      color:#fff;
      padding-top:2px;
      font-family: Roboto Medium;
      font-size: 10px;
    }
    &:hover {
      filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
      -moz-opacity: 0.8;
      -khtml-opacity: 0.8;
      opacity: 0.8;
    }
  }
}
</style>