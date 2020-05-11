<template>
  <div id="app">
    <router-view></router-view>
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <van-button type="primary" >测试</van-button> -->
    <van-tabbar route>
      <van-tabbar-item replace to="/" icon="home-o">
        首页
      </van-tabbar-item>
      <van-tabbar-item replace to="/add" icon="plus">
        发布
      </van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import { Button, Tabbar, TabbarItem } from 'vant'


export default {
  name: 'App', 
  components: {
    // HelloWorld
    [Button.name]: Button,
    [Tabbar.name]: Tabbar,
    [TabbarItem.name]: TabbarItem

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
</style>
