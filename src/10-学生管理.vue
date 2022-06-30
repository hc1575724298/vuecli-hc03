<!--
 * @Descripttion: 
 * @version: 
 * @Author: suiyue
 * @email: 1373842098@qq.com
 * @Date: 2022-06-30 21:12:19
 * @LastEditors: sj
 * @LastEditTime: 2022-06-30 22:41:31
-->
<template>
  <div id="app">
    <div>
      <span>姓名:</span>
      <input type="text" v-model.trim="name"/>
    </div>
    <div>
      <span>年龄:</span>
      <input type="number" v-model.trim="age"/>
    </div>
    <div>
      <span>性别:</span>
      <select v-model.trim="sex">
        <option value="男">男</option>
        <option value="女">女</option>
      </select>
    </div>
    <div>
      <button @click="addFn()">添加/修改</button>
    </div>
    <div>
      <table
        border="1"
        cellpadding="10"
        cellspacing="0"
      >
        <tr>
          <th>序号</th>
          <th>姓名</th>
          <th>年龄</th>
          <th>性别</th>
          <th>操作</th>
        </tr>
        <tr v-for="(item,index) in list" :key="index">
          <td>{{index+1}}</td>
          <td>{{item.name}}</td>
          <td>{{item.age}}</td>
          <td>{{item.sex}}</td>
          <td>
            <button @click="del(index)">删除</button>
            <button @click="editFn(index)">编辑</button>
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return {
      list:[
        {name:'zs',age:18, sex:'男'}
      ],
      name:'',
      age: 0,
      sex:'',
      edit:true,
      editId:0
    }
  },
  methods:{
    addFn(){
      if(this.name==''||this.age==0||this.sex=='')return alert('请填写完整')
      if(this.age <=0) return alert('请输入正确的年龄')
      if(this.edit){
        this.list.push({
        name: this.name,
        age:this.age,
        sex: this.sex,
      })
      }
      else{
        this.list[this.editId].name=this.name
        this.list[this.editId].age=this.age
        this.list[this.editId].sex=this.sex      
          this.name=''
         this.age=0
          this.sex=''
          this.edit=true
      }
      this.name=''
      this.age=0
      this.sex=''
     
    },
    editFn(val){
      
      this.name=this.list[val].name
      this.age=this.list[val].age
      this.sex=this.list[val].sex 
      this.edit=false
      this.editId=val
    },
    del(val){
      this.list.splice(val, 1)
    }
  }
}
</script>

