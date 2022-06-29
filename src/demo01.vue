<template>
  <div>
    <div>
      <div>
        <span>选择所在地区：</span>
        <input type="radio" value=1 name="area" v-model="area"/>中国大陆
        <input type="radio" value=2 name="area" v-model="area" />中国香港
      </div>
      <div>
        <span>手机号码：</span>
        <input type="text" v-model.number="phope"/>
      </div>

      <div>
        <span>年龄</span>：
        <input type="text"  v-model.number="age"/>
      </div>
      <div>
        <span>密码</span>：
        <input type="password" v-model="paw" />
      </div>

      <div>
        <span>爱好：</span>
        <input type="checkbox" value="看书"  v-model="val"/>看书
        <input type="checkbox" value="学习"   v-model="val"/>学习
        <input type="checkbox" value="写代码"   v-model="val"/>写代码
        <input type="checkbox" value="游戏"   v-model="val"/>游戏
      </div>
      <div><input type="checkbox"   v-model="istrue"/> 记住密码</div>
      <div>===============================================</div>
      <div>
        我来自：{{["中国大陆","中国香港"][area]}}
        <br />
        手机号码是：{{phope}}
        <br />
        年龄是：{{age}}
        <br />
        密码是：{{paw}}
        <br />
        爱好是：{{val.join(',')}}
        <br />
        是否记住密码：{{istrue?'是':'否'}}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
        area:1,
        phope:'',
        age:'',
        paw:'',
        val:['看书','学习','写代码'],
        istrue:true
    }
  },
}
</script>

<style></style>
