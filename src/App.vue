<!-- App.vue文件是项目入口组件、全局容器（相当于 “整个 App 的外壳”） -->

<template>
  <div id="app">
    <!-- 头部区域 -->
    <div style="height:60px;line-height: 60px;background-color: white;margin-bottom: 2px;">
      <img src="@/assets/logo.png" alt="网站logo" style="width:50px;position: relative;top:5px;left:10px">
      <!-- position: relative;让元素相对于在父类容器中自身原始位置进行偏移，且不脱离文档流 -->
      <span style="position: relative;left:20px;bottom:8px;font-size: 34px;">图书管理系统</span>
    </div>

    <!-- 侧边栏和主体 -->
    <div style="display: flex;">
      <!-- 侧边栏导航） -->
      <div style="width: 200px;min-height:calc(100vh - 62px); overflow: hidden; margin-right: 2px;background-color: white;">
        <el-menu :default-active="$route.path" :default-openeds="['/']" router class="el-menu-demo">
          <el-menu-item index="/">
            <i class="el-icon-s-home"></i>
            <span>首页</span>
          </el-menu-item>
          <el-submenu index="/">
            <template slot="title">我的工作台</template>
            <el-menu-item index="about">
              <i class="el-icon-info"></i>
              <span>关于</span>
            </el-menu-item>
          </el-submenu>
        </el-menu>
      </div>

      <!-- 主体数据 -->
      <div style="flex:1;background-color: white;padding:10px">
        <router-view /> <!-- 展示路由到的界面 -->
      </div>

    </div>

  </div>
</template>
