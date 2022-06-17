<template>
 <div style="padding: 10px">
   <div style="magin:10px 0">
     <el-button type="primary">查询</el-button>
   </div>

   <el-table :data="tableData" border stripe style="width: 100%">
<!--     等待填充数据-->
   </el-table>

<!--   翻页、跳转条-->
   <div style="margin: 10px 0">
     <el-pagination
       v-model:current-page="currentPage"
       v-model:page-size="pageSize4"
       :page-sizes="[5, 10, 20]"
       :small="small"
       :disabled="disabled"
       :background="background"
       layout="total, sizes, prev, pager, next, jumper"
       :total="total"
       @size-change="handleSizeChang"
       @current-change="handleCurrentChange"
     />
   </div>
 </div>
</template>

<script>
export default {
  name: "data_viewer"
}
</script>

<style scoped>

</style>