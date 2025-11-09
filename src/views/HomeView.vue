<!-- 具体业务页面（相当于 “首页这个具体页面”） -->


<!-- vue要求template标签下只能有一个根元素（如div等） -->
<template>
  <div>
    <!-- 搜索表单 -->
    <el-input style="width:240px;margin-left: 5px;" placeholder="请输入名称"></el-input>
    <el-input style="width:240px;margin-left: 5px;" placeholder="请输入联系方式"></el-input>
    <el-button type="primary" round style="margin-left: 5px;">
      <i class="el-icon-search">搜索</i>
    </el-button>

    <el-table :data="tableData" stripe>
      <el-table-column prop="name" label="名称"></el-table-column>
      <el-table-column prop="age" label="年龄"></el-table-column>
      <el-table-column prop="address" label="地址"></el-table-column>
      <el-table-column prop="phone" label="联系方式"></el-table-column>
    </el-table>


    <!-- 分页 -->
    <div style="margin-top: 20px;">
      <el-pagination background layout="prev, pager, next" :page-size="5" :total="100">
      </el-pagination>
    </div>

  </div>
</template>

<script>

export default {
  name: 'HomeView',
  data() {
    return {
      tableData: [
        { name: '唐三', age: 20, address: '汕头', phone: '18318212567' },
        { name: '唐三', age: 20, address: '汕头', phone: '18318212567' },
        { name: '唐三', age: 20, address: '汕头', phone: '18318212567' },
        { name: '唐三', age: 20, address: '汕头', phone: '18318212567' },
        { name: '唐三', age: 20, address: '汕头', phone: '18318212567' },
        { name: '唐三', age: 20, address: '汕头', phone: '18318212567' },
      ]
    }
  }
}
</script>
