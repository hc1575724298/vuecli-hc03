<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-30 19:01:21
 * @LastEditors: sj
 * @LastEditTime: 2022-06-30 19:01:21
-->
<template>
  <div>
    <h1>{{ obj.a}}</h1>
    <button @click="change">改变</button>
  </div>
</template>

<script>
export default {
 data(){
  return {
    obj:{
      b:10
    }
  }
 },
 methods:{
  change(){
    // this.obj={
    //   a:99,
    //   b:10
    // }

    this.$set(this.obj,'a',99)
  }
 }
}
</script>

<style>

</style>