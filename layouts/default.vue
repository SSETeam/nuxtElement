<template>
  <div>
    <header>
      <div class="top-bar clearfix">
        <div class="top-bar-l">
          欢迎您！<nuxt-link to='./bonduserinfo'>张三<i class="el-icon-edit"></i></nuxt-link>
        </div>
        <div class="top-bar-r">
          <el-dropdown>
            <span class="el-dropdown-link">
              张三<i class="el-icon-arrow-down el-icon--right"></i>
            </span>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item>退出登录</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </div>
      </div>
      <div class="top-logo">
        <div class="top-logo-bg">
          <h1>
            <img alt="logo" src="../assets/images/logo.png"/>
          </h1>
        </div>
      </div>
      <el-menu :default-active="activeIndex" class="blb-menu" mode="horizontal" 
      @select="handleSelect"
      active-text-color="#1890ff">
        <el-menu-item index="1">首页</el-menu-item>
        <el-submenu index="2" popper-class="blb-menu-item">
          <template slot="title">我的工作台</template>
          <el-menu-item index="2-1">选项1</el-menu-item>
          <el-menu-item index="2-2">选项2</el-menu-item>
          <el-menu-item index="2-3">选项3</el-menu-item>
          <el-submenu index="2-4">
            <template slot="title">选项4</template>
            <el-menu-item index="2-4-1">选项1</el-menu-item>
            <el-menu-item index="2-4-2">选项2</el-menu-item>
            <el-menu-item index="2-4-3">选项3</el-menu-item>
          </el-submenu>
        </el-submenu>
        <el-menu-item index="3">消息中心</el-menu-item>
      </el-menu>
    </header>
      <div class="blb-breadcrumb">
        <el-breadcrumb separator="/">
          <el-breadcrumb-item>首页</el-breadcrumb-item>
          <el-breadcrumb-item>活动详情</el-breadcrumb-item>
        </el-breadcrumb>
      </div>
      <nuxt/>
      <footer class="blb-footer">
         <div>窗前明月光，关顾感光鼓逛逛逛光光光光光</div>
         <div>窗前明月光，关顾感光鼓逛逛逛光光光光光</div>
         <div>窗前明月光，关顾感光鼓逛逛逛光光光光光</div>
      </footer>
  </div>

</template>
<script>
  export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>


