<template>
  <div class="direct">
    <div class="wrapper">
      <div class="header-contact-list">
        <input type="text" name="" id="" placeholder="Поиск по имени" class="inp-search-contact-list">
        <a href="#"></a>
      </div>
      <div class="header-chat">
        <a href="#" class="link-avatar-drop">
          <div class="conteanr-avatar-drop">
            <img src="@/assets/photo/id-1/1.jpeg" alt="">
          </div>
        </a>
        <a href="#" class="name">Анастасия глупая, 24</a>
        <a href="#" class="thr"></a>
      </div>
      <div class="wrapper-contact-list">
        <div class="contact-list">
          <a href="#" class="contact">
            <div class="avatar">
              <img src="@/assets/photo/id-1/1.jpeg" alt="">
            </div>
            <span class="status online"></span>
            <span class="status-text">On-line</span>
            <p class="name">Анастасия глупая, 24</p>
            <p class="last-message">Привет, как дела? Я Настя. Давай дружить? Тут находится последнее сообщение, сколько влезет, обрезается автоматически</p>
            <span class="message-counter">9+</span>
            <span class="date-last-message">12.06.21</span>
          </a>
          <a href="#" class="contact">
            <div class="avatar">
              <img src="@/assets/photo/id-1/5.jpeg" alt="">
            </div>
            <span class="status offline"></span>
            <span class="status-text">Бала 5 минут назад</span>
            <p class="name">Кристина, 18</p>
            <p class="last-message">Добрый день) не против знакомства?)</p>
            <span class="message-counter">1</span>
            <span class="date-last-message">11.06.21</span>
          </a>
        </div>
      </div>
      <div class="wrapper-chat">
        <div class="chat">
          <p class="date">10 августа 2021 г.</p>
          <p class="message send">Привет, познакомимся? <span>14:45</span></p>
          <p class="message send">Меня зовут, бла бла бла, это текст ссообщения и тд, как считаешь оно отправилось и ты его прочитала? <span>14:45</span></p>
          <p class="message send">? <span>14:45</span></p>
          <p class="message receive">Да да, всё дошло. Я всё вижу и прочитала <span>14:45</span></p>
          <p class="message receive">Бал бла бал <span>14:45</span></p>
        </div>
        <div class="conteaner-writing-message">
          <label for="ex1" class="label-sender">
            <textarea name="ex1" id="ex1" class="sender" rows="1" placeholder="Напишите сообщение..." autofocus></textarea>
            <a href="#" class="btn-smile" @click="smile = !smile"></a>
            <!-- Как только пользователь начал писать текст, строчка ниже, её класс, btn-send-message, должен менять display:none, на display:block. -->
            <!-- И если сообщение стёрто до 0 символов или отправлено то display:block на должен менять display:none -->
            <a href="#" class="btn-send-message" style="display:block !importan"><span>Отправить</span></a>
            <a href="#" class="btn-like"></a>
            <a href="#" class="btn-phote"></a>
          </label>
          <div class="conteaner-choosing-smile" :class="{ smile }">
            <span class="emoji">&#128512;</span>
            <span class="emoji">&#128521;</span>
            <span class="emoji">&#128513;</span>
            <span class="emoji">&#128518;</span>
            <span class="emoji">&#128517;</span>
            <span class="emoji">&#128514;</span>
            <span class="emoji">&#129315;</span>
            <span class="emoji">&#128522;</span>
            <span class="emoji">&#128578;</span>
            <span class="emoji">&#128516;</span>
            <span class="emoji">&#128579;</span>
            <span class="emoji">&#128519;</span>
            <span class="emoji">&#128515;</span>
            <span class="emoji">&#128538;</span>
            <span class="emoji">&#129392;</span>
            <span class="emoji">&#128537;</span>
            <span class="emoji">&#128525;</span>
            <span class="emoji">&#128535;</span>
            <span class="emoji">&#128536;</span>
            <span class="emoji">&#129321;</span>
            <span class="emoji">&#128523;</span>
            <span class="emoji">&#128539;</span>
            <span class="emoji">&#128540;</span>
            <span class="emoji">&#129322;</span>
            <span class="emoji">&#128541;</span>
            <span class="emoji">&#129297;</span>
            <span class="emoji">&#129300;</span>
            <span class="emoji">&#129325;</span>
            <span class="emoji">&#129303;</span>
            <span class="emoji">&#129323;</span>
            <span class="emoji">&#128528;</span>
            <span class="emoji">&#128566;</span>
            <span class="emoji">&#129320;</span>
            <span class="emoji">&#128556;</span>
            <span class="emoji">&#128527;</span>
            <span class="emoji">&#128529;</span>
            <span class="emoji">&#128530;</span>
            <span class="emoji">&#128580;</span>
            <span class="emoji">&#129296;</span>
            <span class="emoji">&#129317;</span>
            <span class="emoji">&#128524;</span>
            <span class="emoji">&#128532;</span>
            <span class="emoji">&#128554;</span>
            <span class="emoji">&#128564;</span>
            <span class="emoji">&#129316;</span>
            <span class="emoji">&#129398;</span>
            <span class="emoji">&#129319;</span>
            <span class="emoji">&#128567;</span>
            <span class="emoji">&#129327;</span>
            <span class="emoji">&#129396;</span>
            <span class="emoji">&#128565;</span>
            <span class="emoji">&#129298;</span>
            <span class="emoji">&#129397;</span>
            <span class="emoji">&#129326;</span>
            <span class="emoji">&#129301;</span>
            <span class="emoji">&#129314;</span>
            <span class="emoji">&#129312;</span>
            <span class="emoji">&#129395;</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'Direct',
  components: {
  
  },
  data() {
    return {
      smile: true
    }
  }
}
</script>
<style scoped lang="scss">
.direct {
  display: grid;
  position: relative;
  height: 1fr;
  width: 1fr;
  .wrapper {
    display: grid;
    position: absolute;
    margin:20px auto 0;
    width:950px;
    height: calc(100% - 30px);
    grid-template-columns: 330px 1fr;
    grid-template-rows: 50px 1fr;
    border:1px solid #e4e9f2;
    border-radius: 22px;
    padding:0;
    overflow: hidden;
    .header-contact-list {
      border:1px;
      border-style: none solid solid none;
      border-color: #e4e9f2;
      box-sizing:border-box;
      .inp-search-contact-list {
        float:left;
        width:230px;
        height:30px;
        border-radius: 30px;
        border:2px solid #e4e9f2;
        background-color: #fff;
        outline:none;
        box-sizing:border-box;
        padding:0 14px;
        font-size: 14px;
        margin:10px 0 0 20px;
        font-family: Roboto Regular;
        transition: .3s;
        &:focus, &:hover {
          border:2px solid #111;
        }
        &::placeholder {
          color:#999;
          font-style: italic;
        }
      }
      a {
        float:right;
        width:30px;
        height:20px;
        text-decoration: none;
        margin:15px 5px 0 0;
        background-image: url(~@/assets/images/three-dots.svg);
        background-size: 21px;
        background-position: 0px 0px;
        background-repeat: no-repeat;
        &:hover {
          filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
          -moz-opacity: 0.8;
          -khtml-opacity: 0.8;
          opacity: 0.8;
        } 
      }
    }
    .wrapper-contact-list {
      display: grid;
      padding:0px;
      margin:0px;
      height:100%;
      box-sizing:border-box;
      overflow: hidden;
      .contact-list {
        display: grid;
        position: relative;
        overflow-y: scroll;
        align-content: start;
        &::-webkit-scrollbar {
          width: 1px;
          background: #e4e9f2;
        }
        &::-webkit-scrollbar-thumb {
          background-color: #999;
        }
        .contact {
          position: relative;
          width:100%;
          margin: 0 0 0 0;
          height: 114px;
          background: #f9f9fb;
          transition: .3s;
          overflow: hidden;
          border: 1px;
          border-style: none none solid none;
          border-color: #e4e9f2;
          &:hover {
            background: #f0f4f9;
          }
          &.active {
            background: #f0f4f9 !important;
          }
          .avatar {
            position: absolute;
            top:15px;
            left:20px;
            width:42px;
            height:42px;
            border-radius: 42px;
            overflow: hidden;
            img {
              width:100%;
            }
          }
          .name {
            position: absolute;
            top:35px;
            left:80px;
            overflow: hidden;
            width:214px;
            height:20px;
            color:#111;
            font-family: Roboto Medium;
            font-size: 14px;
          }
          .last-message {
            position: absolute;
            top:60px;
            left:80px;
            overflow: hidden;
            width:210px;
            height:36px;
            color:#555;
            font-family: Roboto Regular;
            font-size: 13px;
            line-height: 17px;
          }
          .status {
            position: absolute;
            top:20px;
            left:54px;
            border-radius: 10px;
            width:8px;
            height:8px;
            border:2px solid #f9f9fb;
            &.online {
              background: #67bc0f;
            }
            &.offline {
              background: #b8b7b7;
            }
          }
          .status-text {
            position: absolute;
            top:20px;
            left:80px;
            font-family: Roboto Medium;
            font-size: 11px;
            color: #999;
          }
          .date-last-message {
            position: absolute;
            bottom:3px;
            right:3px;
            font-family: Roboto Regular;
            font-size: 11px;
            color: #afafaf;
          }
          .message-counter {
            float:right;
            display: block;
            margin: 10px 10px 0 0;
            width:30px;
            height:30px;
            border-radius: 18px;
            color:#fff;
            background: #f35554;
            font-family: Roboto Bold;
            font-size: 11px;
            text-align: center;
            padding: 9px;
            box-sizing: border-box;
          }
        }
      }
    }
    .header-chat {
      position: relative;
      border:1px;
      border-style: none none solid none;
      border-color: #e4e9f2;
      .link-avatar-drop {
        position:absolute;
        width:28px;
        height:28px;
        top:12px;
        left:30px;
        .conteanr-avatar-drop {
          position: relative;
          width:28px;
          height:28px;
          overflow: hidden;
          border-radius: 30px;
          background-color: #d0d1d3;
          background-image: url(~@/assets/images/avatar-drop.svg);
          background-size: 24px;
          background-position: center 8px;
          background-repeat: no-repeat;
          transition: .3s;
          img {
            width:100%;
          }
        }
      }
      .name {
        position: absolute;
        text-decoration: none;
        top:17px;
        left:70px;
        display: block;
        width:430px;
        height:20px;
        overflow: hidden;
        color:#313131;
        font-family: Roboto Medium;
        font-size: 15px;
      }
      .thr {
        float:right;
        width:30px;
        height:20px;
        text-decoration: none;
        margin:15px 15px 0 0;
        background-image: url(~@/assets/images/three-dots.svg);
        background-size: 21px;
        background-position: 0px 0px;
        background-repeat: no-repeat;
        &:hover {
          filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
          -moz-opacity: 0.8;
          -khtml-opacity: 0.8;
          opacity: 0.8;
        } 
      }
    }
    .wrapper-chat {
      display: grid;
      position: relative;
      height:1fr;
      padding: 0;
      grid-template-rows: 1fr auto;
      overflow: hidden;
      .chat {
        padding: 30px;
        width: 614px;
        margin-top: 3px;
        box-sizing: border-box;
        overflow-y: auto;
        display: flex;
        height: 1fr;
        flex-direction: column;
        &::-webkit-scrollbar {
          width: 6px;
        }
        &::-webkit-scrollbar-thumb {
          background-color: #efefef;
          border-radius: 10px;
        }
        .date {
          position: relative;
          display: block;
          width: 100%;
          height: 20px;
          color:#8e8e8e;
          font-family: Roboto Regular;
          font-size: 12px;
          text-align: center;
          padding: 30px 0;
        }
        .message {
          height:auto;
          display: block;
          position: relative;
          line-height: 18px;
          font-family: Roboto Regular;
          font-size: 14px;
          border-radius: 14px;
          color: #111;
          &.send {
	          background: #d8ebff;
            align-self: flex-end;
            margin:2px 0px;
            max-width: 415px;
            min-width:32px;
            padding: 8px 12px 23px;
            span {
              position: absolute;
              right:17px;
              bottom:3px;
              color:#ababab;
              font-size: 12px;
              transition: .3s;
            }
          }
          &.receive { 
	          background: #efefef;
            align-self: flex-start;
            margin:2px 0;
            max-width: 415px;
            min-width:32px;
            padding: 10px 17px 27px;
            span {
              position: absolute;
              right:17px;
              bottom:8px;
              color:#9f9f9f;
              font-size: 12px;
              transition: .3s;
            }
          }
        }
      }
      .conteaner-writing-message {
        position: relative;
        width:590px;
        height:min-content;
        .label-sender {
          display: block;
          position: relative;
          width:550px;
          min-height:41px;
          border:1px solid #bac5c5;
          margin:20px 0 20px 30px;
          padding:0;
          border-radius: 40px;
          outline:none;
          overflow: hidden;
          .sender {
            position: relative;
            width:380px;
            min-height:18px;
            margin:12px 0 0 55px;
            border:1px solid #fff;
            padding:0;
            resize: none;
            font-family: Roboto Regular;
            font-size: 14px;
            color:#313131;
            outline:none;
            &::-webkit-scrollbar {
              width: 6px;
            }
            &::-webkit-scrollbar-thumb {
              background-color: #d4d4d4;
              border-radius: 10px;
            }
          }
          .btn-smile {
            position: absolute;
            display: block;
            width: 36px;
            height: 36px;
            background-image: url(~@/assets/images/smile.svg);
            background-size: 23px;
            background-position: 6px 6px;
            background-repeat: no-repeat;
            top: 50%;
            left: 5px;
            margin-top: -18px;
          }
          .btn-send-message {
            position:absolute;
            // Нужно поменять на display: block; как только пользователь начал писать текст,
            // и меняем обратно на display: none; как только сообщение отправлено или стёрно полностью.
            display: none;
            z-index: 9;
            top:0;
            right:0;
            bottom:0;
            width:100px;
            text-align: center;
            color:#fe2c55;
            background-color: #fff;
            text-decoration: none;
            font-family: Roboto Medium;
            font-size: 14px;
            span {
              position: absolute;
              display: block;
              width:100%;
              height:18px;
              top: 50%;
              margin-top: -8px;
            }
          }
          .btn-like {
            position: absolute;
            display: block;
            width: 36px;
            height: 36px;
            background-image: url(~@/assets/images/like.svg);
            background-size: 28px;
            background-position: 4px 4px;
            background-repeat: no-repeat;
            top: 50%;
            right: 5px;
            margin-top: -18px;
          }
          .btn-phote {
            position: absolute;
            display: block;
            width: 36px;
            height: 36px;
            background-image: url(~@/assets/images/photo.svg);
            background-size: 28px;
            background-position: 4px 4px;
            background-repeat: no-repeat;
            top: 50%;
            right: 50px;
            margin-top: -18px;
          }
          .btn-smile:hover, .btn-like:hover, .btn-phote:hover {
            filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
            -moz-opacity: 0.8;
            -khtml-opacity: 0.8;
            opacity: 0.8;
          }
        }
        .conteaner-choosing-smile {
          position: absolute;
          display: grid;
          width:300px;
          height:400px;
          border-radius: 14px;
          box-shadow:0 0 30px 0 rgba(0, 0, 0, 0.15);
          bottom:62px;
          left:12px;
          background: #fff;
          grid-template-columns: auto auto auto auto auto;
          gap: 5px;
          overflow-y: auto;
          padding:10px;
          box-sizing:border-box;
          &::-webkit-scrollbar {
            width: 6px;
          }
          &::-webkit-scrollbar-thumb {
            background-color: #d4d4d4;
            border-radius: 10px;
          }
          &::after {
            content: '';
            position: absolute;
            margin:0;
            bottom:-8px;
            left:24px;
            width: 0; 
            height: 0;
            border-left: 8px solid transparent;
            border-right: 8px solid transparent;
            border-top: 8px solid #fff;
          }
          .emoji {
            display: block;
            position: relative;
            font-size: 35px;
            cursor: pointer;
            transition: .3s;
            &:hover {
              filter:progid:DXImageTransform.Microsoft.Alpha(opacity=80);
              -moz-opacity: 0.8;
              -khtml-opacity: 0.8;
              opacity: 0.8;
            }
          }
        }
        .smile {
          display: none;
        }
      }
    }
  }
}
</style>