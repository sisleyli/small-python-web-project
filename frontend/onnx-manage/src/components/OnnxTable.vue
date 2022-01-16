<template>
  <div>
    <el-header style="text-align: right; font-size: 12px">
      <el-menu
        :default-active="headerItem"
        mode="horizontal"
        @select="handleSelect"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b"
      >
        <el-menu-item index="1">模型列表</el-menu-item>
        <el-menu-item index="2">模型详情</el-menu-item>
      </el-menu>
    </el-header>
    <el-table  v-if="headerItem === '1'" class="table" :data="tableData">
      <el-table-column prop="date" label="日期" width="140"> </el-table-column>
      <el-table-column prop="name" label="姓名" width="120"> </el-table-column>
      <el-table-column prop="address" label="地址"> </el-table-column>
    </el-table>
  </div>
</template>


<script>
  const item = {
    date: "2016-05-02",
    name: "王小虎",
    address: "上海市普陀区金沙江路 1518 弄",
  };
export default {
  data() {
    return {
      tableData: Array(20).fill(item),
      headerItem: "1",
      asideItem: "1",
    };
  },
  methods: {
    handleSelect(index, indexPath) {
      console.log(index, indexPath);
      this.headerItem = "" + index;
    },
  },
};
</script>

<style scoped>
.table {
  margin: 8px;
}
.el-header {
  color: #333;
  line-height: 60px;
  padding: 0;
}
.el-menu {
  border-right: 0;
}
.el-aside {
  color: #333;
}
</style>