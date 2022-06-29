<template>
  <div>
    <!-- 1. 绑定键盘按下事件.enter-回车 
         2. .esc修饰符 - 取消键-->
    <input type="text" @keyup.enter="enter" />
    <hr />
    <input type="text" @keyup.esc="esc" />
     <hr />
    <input type="text" @keyup="fn" />
  </div>
</template>

<script>
export default {
  methods: {
    enter() {
      alert('enter')
    },
    esc() {
      alert('esc')
    },
    fn(e){
      if(e.keyCode == 13){
         alert('老版本keyCode')
      }
    }
  },
}
</script>

<style></style>
