<template>
  <div>
    <p>你要购买商品的数量:{{count}}</p>
    <button @click="addFn">+1</button>
    <button v-on:click="addFn">+1</button>
    <button @click="addCountFn(5)">+5</button>
    <button @click="subFn">减少1</button>
  </div>
</template>

<script>
export default {
  name: 'VuecliDemo03',

  data() {
    return {
      count:0
    }
  },

  mounted() {},

  methods: {
    addFn() {
      // this代表export default后面的组件对象(下属有data里return出来的属性)
      this.count++
      // this 要注意一下
    },
    addCountFn(num) {
      this.count += num
    },
    subFn() {
      this.count--
    },
  },
}
</script>

<style lang="scss" scoped></style>
