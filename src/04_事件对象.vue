<template>
  <div>
    <!-- 1. 事件触发, 无传值, 可以直接获取事件对象
    2. 事件触发, 传值, 需要手动传入$event -->
    <a href="http://www.baidu.com" @click="one">百度</a>
    <hr />
    <a href="http://www.taobao.com" @click.prevent="two(5, $event)">淘宝</a>
  </div>
</template>

<script>
export default {
  name: 'VuecliDemo04',

  data() {
    return {}
  },

  mounted() {},

  methods: {
    one(e) {
      e.preventDefault()
    },

    two(val, e) {
      console.log(val)
      console.log(e)
    },
  },
}
</script>

<style scoped></style>
