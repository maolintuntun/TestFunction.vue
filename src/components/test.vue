<!-- 这是一个单文件组件 单文件组件分为三个部分 -->

<template>
  <!-- template放置的是DOM结构，模板，或者是 视图区域 -->
  <h2 class="red">test...{{ msg }}</h2>
</template>

<script>
// script是脚本区域
// 为这个组件声明这个组件的属性（props)、数据、方法
export default {
  name: 'HelloWorld',

  //props是这个组件的属性
  props: {
    msg: {
      //类型
      type: String,
      //默认值
      default: ' test msg',
    },
  },
  //注册这个组件对应的方法
  methods: {},

  //注册这个组件对应的数据
  data() {
    return {}
  },
}
</script>

<style>
/*style是样式区域,可以声明一些样式*/

/* 例如将这个h2标题的颜色设为红色的*/
.red {
  color: #ff0000;
}
</style>

<!-- 在定义好了这个组件之后，就可以去app.vue里面，对这个组件进行引入，和注册！！！ -->
