<template>
    <el-menu default-active="active" 
            class="el-menu-demo"
            mode="horizontal"
            @select="handleSelect"
            background-color="#545c64"
            text-color="#fff"
            active-text-color="#ffd04b">
        <el-menu-item index="0"><img src="http://www.ladis.com.cn/a_images/public/logo.png"></el-menu-item>
      <el-menu-item index="3" class="menu-f menu-font" >帮助</el-menu-item>      
      
      <el-submenu index="2" class="menu-f menu-font">
          <template slot="title">设备</template>
          <el-menu-item index="2-1" class="menu-font">ups</el-menu-item>
          <el-menu-item index="2-2" class="menu-font" >空调</el-menu-item>
          <el-menu-item index="2-3" class="menu-font" >io</el-menu-item>
      </el-submenu>
      <el-menu-item index="1" class="menu-f menu-font">用户</el-menu-item>
    </el-menu>
</template>

<script>
export default {
    name:'ehead',

    methods:{
        handleSelect(){
            
        }
    }
}
</script>

<style scoped>
  
  .menu-f{
      float: right;      
  }
  .menu-font{
      font-size: 18px
  }
</style>

