<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <test></test>

    <!-- 按钮组件的复用，一次可以new好几个按钮 -->
    <!-- &nbsp；是空格的意思 -->
    <button-counter></button-counter>&nbsp;
    <button-counter></button-counter>&nbsp;
    <button-counter></button-counter>
  </div>
</template>

<script>
import ButtonCounter from './components/button-counter.vue'
//通过import语法，引入刚刚做好的test组件
import HelloWorld from './components/HelloWorld.vue'
import test from './components/test.vue'

//引入好了之后，在components内进行局部注册.之后就能在第五行的div里调用test标签了
export default {
  name: 'App',
  components: {
    HelloWorld,
    test,
    ButtonCounter,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #3e5974;
  margin-top: 60px;
}
</style>
