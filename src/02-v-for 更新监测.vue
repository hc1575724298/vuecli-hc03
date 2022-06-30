<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-30 18:55:39
 * @LastEditors: sj
 * @LastEditTime: 2022-06-30 18:55:39
-->
<template>
  <div>
    <ul>
      <li v-for="item in arr" :key="item">{{item}}</li>
    </ul>
    <button @click="resFn">翻转数组</button>
    <button @click="sliceFn">截取前三个</button>
    <button @click="change">更新第一个值</button>
  </div>
</template>

<script>
export default {
data(){
  return{
    arr:[1,2,3,4,5]
  }
},
methods:{
  resFn(){
    this.arr.reverse()
  },
  sliceFn(){
    this.arr = this.arr.slice(0,3)
  },
change(){
  this.$set(this.arr,0,999)
}
}
}
</script>

<style>

</style>