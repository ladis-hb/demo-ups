<template>
  <div id="app">
    <ehead></ehead>
    <el-container>
      <el-aside width="200px">
        <easide></easide>
      </el-aside>

      <el-container>
        <el-main>
          <emain></emain>
        </el-main>
      </el-container>

    </el-container>
    
  </div>
</template>

<script>
import ehead from './components/head.vue'
import easide from './components/asid.vue'
import emain from  './components/main'

export default {
  name: 'app',
  components: {
    ehead,
    easide,
    emain,
  }
}
</script>

<style>

</style>
