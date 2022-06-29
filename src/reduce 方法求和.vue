<template>
  <div id="app">
    <p>{{ fn() }}{{ cunt }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: [{ a: 100 }, { a: 20 }, { a: -10 }],
      cunt: 0,
    }
  },
  methods: {
    fn() {
      const sum = this.arr.reduce(function (previousValue, currentValue) {
        return currentValue.a + previousValue
      }, 0)
      this.cunt = sum
    },
  },
}
</script>

<style scoped></style>
