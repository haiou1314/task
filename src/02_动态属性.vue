<template>
  <div>
    <a :href="baidu">百度</a>
    <img :src="imgurl" alt="">
    <img :src="img" alt="">
    <img :src="img1" alt="">
  </div>
</template>

<script>
// http://yun.itheima.com/Upload/./Images/20210412/60741c11ab77b.jpg
import img1 from './assets/logo.png'
export default {
  name: 'VuecliDemo02',

  data() {
    return {
      imgurl:'http://yun.itheima.com/Upload/./Images/20210412/60741c11ab77b.jpg',
      baidu:"https://www.baidu.cm",
      img:img1
    };
  },

  mounted() {
    
  },

  methods: {
    
  },
};
</script>