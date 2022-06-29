<template>
  <div class="container">
    <div class="imglist">
      <h3>图片列表区</h3>
      <img src="./assets/03.jpg" alt="" @mouseover="fn(1)" @click="add(1,$event)"/>
      <img src="./assets/04.jpg" alt="" @mouseover="fn(2)" @click="add(2,$event)"/>
      <img src="./assets/05.jpg" alt="" @mouseover="fn(3)" @click="add(3,$event)"/>
    </div>
    <div class="show">
      <h3>图片预览区</h3>
      <img :src="cuent" alt="" style="width: 600px; height: auto" />
    </div>
    <div></div>
  </div>
</template>

<script>
import img1 from './assets/03.jpg'
import img2 from './assets/04.jpg'
import img3 from './assets/05.jpg'
export default {
  data() {
    return {
      cuent: img1,
    }
  },
  methods: {
    fn(val) {
      this.cuent = { 1: img1, 2: img2, 3: img3 }[val]
    },
    add(val,e){
        alert("第"+val+'图：地址：'+e.target.src)
    }
  },
}
</script>

<style scoped>
.container {
  display: flex;
}
.imglist {
  border: 2px solid red;
}
.imglist img {
  width: 200px;
  height: auto;
}
.show {
  border: 2px solid red;
  margin-right: 20px;
}
</style>
