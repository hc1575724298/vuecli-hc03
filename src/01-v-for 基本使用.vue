<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-30 18:04:03
 * @LastEditors: sj
 * @LastEditTime: 2022-06-30 18:04:03
-->
<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-30 17:44:45
 * @LastEditors: sj
 * @LastEditTime: 2022-06-30 18:02:47
-->
<template>
  <div>
    <ul>
      <li v-for="item in arr" :key="item">{{item}}</li>
    </ul>
    <p v-for="item in stuArr" :key="item.id">
     姓名 {{item.name}}--性别{{item.sex}}--爱好{{item.hobby}}
    </p>
    <div v-for="item in count" :key="item">{{item}}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ["章三", "李四", "迪丽热巴", "xxx"],
      stuArr: [
        {
          id: 1001,
          name: "孙悟空",
          sex: "男",
          hobby: "吃桃子",
        },
        {
          id: 1002,
          name: "猪八戒",
          sex: "男",
          hobby: "背媳妇",
        },
      ],
      tObj: {
        name: "小黑",
        age: 18,
        class: "1期",
      },
      count: 10,
    };
  },
}
</script>

<style>

</style>