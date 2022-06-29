<template>
  <div>
    <div>
      <span>用户名:</span>
      <!-- 1. v-model
         双向数据绑定
         value属性 - vue变量
       -->
      <input type="text" v-model="msg">
    </div>
    <div>
      <span>密码: </span>
      <input type="text" v-bind:value="val" @input="fn">
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      msg:"",
      val:''
    }
  },
  methods: {
    fn(e){
      this.val = e.target.value
    }
  },
}
</script>

<style>

</style>