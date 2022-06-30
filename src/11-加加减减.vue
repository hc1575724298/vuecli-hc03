<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-30 21:18:49
 * @LastEditors: sj
 * @LastEditTime: 2022-06-30 21:18:50
-->
<template>
  <div id="app">
    <ul>
      <li v-for="(item,index) in arr" :key="index">
        <span>{{ item }}</span>
        <button @click="delFn(index)">删除</button>
      </li>
    </ul>
    <button @click="addFn()">生成</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: [5, 7, 1],
    };
  },
  methods: {
   delFn(val){
     this.arr.splice(val, 1);
   },
   addFn(){
     this.arr.push(Math.floor(Math.random() * 10));
   }
  },
};
</script>

<style>
</style>
