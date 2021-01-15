<template>
  <button v-on:click="count++">You clicked me {{ count }} times</button>
</template>

<script>
export default {

  //为什么这个name写不写不影响
  name: 'ButtonCounter',

  //一个组件的data必须是个函数，因此每个实例可以维护一份被返回对象的独立的拷贝。
  //如果vue没有这条规则，点击一个按钮就会影响到其他几个复用的按钮。。。
  data: function() {
    return {
      count: 0,
    }
  },
}
</script>

<style></style>
