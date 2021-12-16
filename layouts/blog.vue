<template>
  <div>
    <div class="wrapper">
      <div class="main">
        <NavigationBlog/>
        <Nuxt/>
      </div>
    </div>
  </div>
</template>
    
<script>
import '@/assets/fonts/roboto/stylesheet.css'
import NavigationBlog from '@/components/Navigation/NavigationBlog.vue'

export default {
  components: {
    NavigationBlog
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Source+Serif+Pro:wght@600&display=swap');

*{
  margin:0;
  padding:0px;
}
html {
  padding:0px;
  height:100%;
}
body {
  position: grid;
  padding: 0;
  margin: 0;
  background: #fbfbfb;
  height:100%;
  // background-image: url(~@/assets/images/fn.png);
  background-position: center top;
  background-repeat: repeat;
}
.additional-navigation-wrapper {
  position: absolute;
  width:100%;
  height:40px;
  top:20px;
  z-index: 99;
  .additional-navigation {
    max-width:1200px;
    min-width:970px;
    height:100%;
    margin: 0 auto;
    padding:0 20px;
    box-sizing:border-box;
    a {
      padding: 7px 20px;
      text-decoration: none;
      width: auto;
      height:31px;
      background: #ced8e7;
      border-radius: 40px;
      box-sizing:border-box;
      font-family: Roboto Medium;
      color:#4e4e81;
      font-size: 15px;
      transition: .3s;
      &.l_f {
        float:left;
      }
      &.r_f {
        float:right;
      }
      &:hover {
        color:#fe2c55;
      }
      &.reg {
        background: none !important;
      }
    }
  }
}
.wrapper {
  padding:15px 0;
  box-sizing:border-box;
  .main {
    display: grid;
    grid-template-rows: auto 1fr;
    min-height: calc(100vh - 30px);
	  background:#fff;
    padding:0;
    width:970px;
    margin:0px auto 0;
    border-radius: 26px;
    box-shadow: 0px 0px 250px 0px rgba(34, 60, 80, 0.08);
    overflow: hidden;
  }
}
</style>