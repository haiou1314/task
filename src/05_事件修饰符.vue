<template>
  <div>
    <div @click="addFn">
      <p @click.stop>.stop - 阻止事件冒泡</p>
      <a @click.stop.prevent href="http://www.baidu.com">去百度</a>
      <p @click.once="fn">点击观察事件处理函数执行几次</p>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    addFn() {
      console.log('father')
    },
    fn(){
      console.log('once');
    }
  },
}
</script>

<style></style>
