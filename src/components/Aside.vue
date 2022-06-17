<template>
  <div>
    <el-menu
        style="width: 200px; min-height: calc(100vh - 50px)"
        :default-active="path"
        router
        class="el-menu-vertical-demo"
        default-openeds="[1]">
      <el-sub-menu index="1">
        <template #title>
          <span>型号管理</span>
        </template>
        <el-menu-item index="/user">电气管理</el-menu-item>
        <el-menu-item index="/book">动力管理</el-menu-item>
      </el-sub-menu>
    </el-menu>
  </div>
</template>

<script>
export default {
  name: "Aside",
  data() {
    return {
      path: this.$router.path // 设置默认高亮的菜单
    }
  }
}
</script>

<style scoped>

</style>