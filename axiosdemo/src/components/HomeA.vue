<template>
    <div class="common-layout">
    <el-container>
      <el-aside width="200px">目录待开发</el-aside>
      <el-container>
        <el-header>炉石竞技场分析</el-header>
        <el-main>
            <CardTableVue></CardTableVue>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import CardTableVue from './CardTable.vue';
export default {
    components:{
        CardTableVue
    }
}
</script>

<style>

</style>