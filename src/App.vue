<template>
  <div id="app">
      <transition name="fade-in">
          <router-view></router-view>
      </transition>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
    }
  }
}
</script>

<style lang="less">
    @import "./common/styles/index.less";
    
    html {
      margin: 0;
      padding: 0;
      height: 100vh;
      box-sizing: border-box;
    }
    body {
      margin: 0;
      padding: 0;
      min-height: 100vh;
      background-color: #f4f4f4;
    }
    * {
      box-sizing: inherit;
      &:before,
      &:after {
        box-sizing: inherit;
      }
    }
    #app{
      width: 100%;
      height: 100%;
        .fade-in-enter-active, .fade-in-leave-active {
            transition: opacity .5s
        }
        .fade-in-enter, .fade-in-leave-to {
            opacity: 0
        }
    }
    img {
      width: 100%;
      height: auto;
      vertical-align: top;
      content: normal !important;
    }
    [aspectratio] {
      position: relative;
    }
    [aspectratio]::before {
      content: '';
      display: block;
      width: 1px;
      margin-left: -1px;
      height: 0;
    }
    [aspectratio-content] {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      width: 100%;
      height: 100%;
    }
</style>
