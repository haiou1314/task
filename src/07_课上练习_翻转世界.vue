<template>
  <div>
    <h1>{{ msg }}</h1>
    <button @click="fn">逆转世界</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: 'hello vue!',
    }
  },
  methods: {
    fn() {
      //this.msg = this.msg.split('').reverse().join('')
      let arr = this.msg.split('')
      arr.reverse()
      this.msg = arr.join('')
    },
  },
}
</script>

<style></style>
