<template>
  <el-container style="height: 100%">
    <el-aside width="200px" style="background-color: rgb(84, 92, 100)">
      <el-menu
        :default-active="asideItem"
        :default-openeds="['1']"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b"
      >
        <el-submenu index="1">
          <template slot="title"><i class="el-icon-menu"></i>ONNX管理</template>
          <el-menu-item-group>
            <el-menu-item index="1-1">查看模型</el-menu-item>
            <el-menu-item index="1-2">上传模型</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
      </el-menu>
    </el-aside>

    <el-container>
      <el-main>
        <onnx-table></onnx-table>
      </el-main>
    </el-container>
  </el-container>
</template>


<script>
import OnnxTable from "./OnnxTable.vue";
export default {
  components: { OnnxTable },
  data() {
    return {
      headerItem: "1",
      asideItem: "1",
    };
  },
};
</script>

<style scoped>
.el-main {
  padding: 0;
}
.el-menu {
  border-right: 0;
}
</style>