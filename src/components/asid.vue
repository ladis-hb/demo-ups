<template>
    <div>
        
    <el-menu default-active="2" class="el-menu-vertical-demo"
    background-color="#909399"
      text-color="#fff"
      active-text-color="#ffd04b">>
      <el-menu-item index="0"><h3>Product</h3></el-menu-item>
        <el-menu-item v-for="(i,key) in list" index="i.id" :key="key">{{i.title}}</el-menu-item>
        <el-menu-item v-for="i of 5" index="i+7" :key="i+7">add</el-menu-item>
    </el-menu>
    </div>
</template>

<script>
export default {
    name:'easide',
    data(){
        return{
            list:[
                {id:1,title:'ups'},
                {id:2,title:'空调'},
                {id:3,title:'电量仪'},
                {id:4,title:'IO'},
                {id:5,title:'温度'},
                {id:6,title:'湿度'},
                {id:7,title:'任务'}
            ]
        }
    }
}
</script>

<style>

</style>

