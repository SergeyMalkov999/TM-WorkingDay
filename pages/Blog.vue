<template>
  <div>
    <div class="blog">
      <a href="#" class="item1">
        <span class="preview-img">
          <img src="@/assets/images/blog/1.jpg" alt="">
        </span>
        <span class="titstat">Парень перестал отвечать на сообщения: почему и что делать?</span>
        <span>Вы познакомились, все было отлично. У вас было одно или даже несколько классных свиданий. Ты уже предвкушаешь развитие отношений и где-то в глубине души надеешься, что новый знакомый – тот самый суженый, уготовленный тебе судьбой. И тут он внезапно пропадает с радаров, перестает отвечать на твои сообщения. Конечно, ты в растерянности,</span>
        <span class="name-categories">Отношения</span>
        <span class="count-read">23434</span>
      </a>
      <a href="#">
        <span class="preview-img">
          <img src="@/assets/images/blog/2.jpg" alt="">
        </span>
        <span class="titstat">10 техник поцелуя, от которых твой парень будет в восторге</span>
        <span class="name-categories">Советы</span>
        <span class="count-read">125354</span>
      </a>
      <a href="#">
        <span class="preview-img">
          <img src="@/assets/images/blog/3.jpg" alt="">
        </span>
        <span class="titstat">Девушка не отвечает на сообщения - что ты сделал не так?</span>
        <span class="name-categories">Всё о сексе</span>
        <span class="count-read">23434</span>
      </a>
      <a href="#">
        <span class="preview-img">
          <img src="@/assets/images/blog/4.jpg" alt="">
        </span>
        <span class="titstat">Что сказать девушке, чтобы она расстаяла. 10 фраз. + Бонус</span>
        <span class="name-categories">БДСМ</span>
        <span class="count-read">18564</span>
      </a>
      <a href="#">
        <span class="preview-img">
          <img src="@/assets/images/blog/5.jpg" alt="">
        </span>
        <span class="titstat">Девушка не хочет офишировать отношения. Что делать и в чём причина? ТОП 10 причин.</span>
        <span class="name-categories">Он и она</span>
        <span class="count-read">3453</span>
      </a>
      <a href="#">
        <span class="preview-img">
          <img src="@/assets/images/blog/6.jpg" alt="">
        </span>
        <span class="titstat">Девушка не хочет офишировать отношения. Что делать и в чём причина? ТОП 10 причин.</span>
        <span class="name-categories">Он и она</span>
        <span class="count-read">3453</span>
      </a>
      <a href="#">
        <span class="preview-img">
          <img src="@/assets/images/blog/7.jpg" alt="">
        </span>
        <span class="titstat">Девушка не хочет офишировать отношения. Что делать и в чём причина? ТОП 10 причин.</span>
        <span class="name-categories">Рейтинги</span>
        <span class="count-read">3453</span>
      </a>
      <a href="#">
        <span class="preview-img">
          <img src="@/assets/images/blog/8.jpg" alt="">
        </span>
        <span class="titstat">Девушка не хочет офишировать отношения. Что делать и в чём причина? ТОП 10 причин.</span>
        <span class="name-categories">Все о сексе</span>
        <span class="count-read">3453</span>
      </a>
      <a href="#">
        <span class="preview-img">
          <img src="@/assets/images/blog/9.jpg" alt="">
        </span>
        <span class="titstat">Девушка не хочет офишировать отношения. Что делать и в чём причина? ТОП 10 причин.</span>
        <span class="name-categories">Он и она</span>
        <span class="count-read">3453</span>
      </a>
    </div>
  </div>
</template>

<script lang="ts">

export default {
  name: 'Blog',
  layout: 'blog',
  components: {

  },
  data() {
    return {
      
    }
  }
}
</script>

<style scoped lang="scss">
.blog {
  text-align: left;
  display: grid;
  margin:0px auto;
  width:850px;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 14px 30px;
  grid-auto-rows: 250px;
  grid-auto-flow: dense;
  padding: 40px 0;
  border: 0px;
  border-style:none none solid none;
  border-color:#ced8e7;
  a {
    display: grid;
    position: relative;
    grid-template-rows: 130px auto 1fr;
    overflow: hidden;
    text-decoration: none;
    border: 1px;
    border-style:none none solid none;
    border-color:#ced8e7;
    .preview-img {
      position: relative;
      width:100%;
      border-radius: 10px;
      overflow: hidden;
      img {
        width:100%;
        height:100%;
        transition: .3s;
        object-fit: cover;
      }
    }
    &:hover {
      width:1fr;
      img {
        transform: scale(1.05);
      }
    }
    .titstat {
      font-family: Roboto Medium;
      color:#111;
      font-size: 13px;
      text-decoration: none;
      line-height: 18px;
      padding:8px 0;
    }
    .name-categories {
      position: absolute;
      bottom:7px;
      left:0;
      border-radius: 30px;
      padding: 2px 10px;
      font-family: Roboto Medium;
      color:#333;
      font-size: 13px;
      background: #f2f2f2;
    }
    .count-read {
      position: absolute;
      bottom:7px;
      right:0;
      border-radius: 30px;
      padding: 2px 10px 2px 28px;
      font-family: Roboto Medium;
      color:#333;
      font-size: 13px;
      background: rgba(255, 255, 255, 0.6);
      background-image: url(~@/assets/images/eye-c2.svg);
      background-size: 18px;
      background-position: 5px 3px;
      background-repeat: no-repeat;
    }
  }
  .item1 {
    display: grid;
    position: relative;
    grid-column: span 2;
    grid-row: span 2;
    grid-template-rows: 250px auto 1fr;
    overflow: hidden;
    text-decoration: none;
    .preview-img {
      position: relative;
      width:100%;
      border-radius: 10px;
      overflow: hidden;
      img {
        width:100%;
        transition: .3s;
      }
    }
    &:hover {
      img {
        transform: scale(1.05);
      }
    }
    .titstat {
      font-family: Roboto Medium;
      color:#111;
      font-size: 24px;
      text-decoration: none;
      line-height: 24px;
      padding:14px 0 10px;
    }
  }
  span {
    font-family: Roboto Regular;
    color:#333;
    font-size: 15px;
    line-height: 19px;
  }
}
</style>