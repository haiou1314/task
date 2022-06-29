<template>
  <div id="app">
    <span>解析前：{{ http }}</span>
    <br />
    <span>解析后:{{ fn() }}</span>
  </div>
</template>

<script>
// http://www.baidu.com?name=zhangsan&age=18&sex=nan#
// 解析出
// {name: 'zhangsan',age: 18, sex: 'nan' }

export default {
  data() {
    return {
      http: 'http://www.baidu.com?name=zhangsan&age=18&sex=nan#',
      obj:{},
    }
  },
  methods: {
    fn() {
      let index = this.http.indexOf('?')
      let last = this.http.indexOf('#')
      let arr = this.http.slice(index + 1, last)
      arr = arr.split('&')
      arr.forEach((item) => {
        this.obj[item.split('=')[0]]=item.split('=')[1]
      })
      return this.obj
    },
  },
}
</script>

<style scoped></style>

