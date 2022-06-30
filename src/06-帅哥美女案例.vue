<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-30 19:40:24
 * @LastEditors: sj
 * @LastEditTime: 2022-06-30 19:40:24
-->
<template>
  <div>
    <ul>
      <li v-for="item in myArr" :key="item">{{item}}</li>
    </ul>
    <button @click="change">走一走</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      myArr: ["帅哥", "美女", "程序猿"],
    };
  },
  methods:{
    change(){
       this.myArr.push(this.myArr[0])
       this.myArr.shift()
    }
  }
}
</script>

<style>

</style>