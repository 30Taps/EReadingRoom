<template>
  <el-container class="home-container">
    <!--头部区域-->
    <el-header>
      <div>
        <img src="../assets/headerlogo.jpg">
        <span>电子阅览室</span>
      </div>
      <el-button type="info" @click="logout">退出</el-button>
    </el-header>
    <!--页面主体区域-->
    <el-container>
      <!--侧边栏-->
      <el-aside width="200px">
        <!--侧边栏菜单区域-->
        <el-menu background-color="#333744"
          text-color="#fff"
          active-text-color="#ffd04b">
          <!--模板-->
          <el-menu-item index="1">
            <!--图标-->
            <i class="el-icon-menu"></i>
            <!--文本-->
            <span slot="title">主页选项一</span>
          </el-menu-item>
          <el-menu-item index="1">
            <!--图标-->
            <i class="el-icon-menu"></i>
            <!--文本-->
            <span slot="title">主页选项二</span>
          </el-menu-item>
          <el-menu-item index="1">
            <!--图标-->
            <i class="el-icon-menu"></i>
            <!--文本-->
            <span slot="title">主页选项三</span>
          </el-menu-item>
          <el-menu-item index="1">
            <!--图标-->
            <i class="el-icon-menu"></i>
            <!--文本-->
            <span slot="title">主页选项四</span>
          </el-menu-item>
        </el-menu>
      </el-aside>
      <!--右侧内容主体-->
      <el-main>登录成功的主页</el-main>
    </el-container>
  </el-container>
</template>

<script>
export default {
  methods: {
    logout () {
      window.sessionStorage.clear()
      this.$router.push('/login')
    }
  }
}
</script>

<style lang="less" scoped>
.home-container {
  height: 100%;
}

.el-header {
  background-color: #373d41;
  display: flex;
  justify-content: space-between;
  padding-left: 0;
  align-items: center;
  color: #fff;
  font-size: 20px;
  > div {
    display: flex;
    align-items: center;
    span {
      margin-left: 15px;
    }
  }
}

.el-aside {
  background-color: #333744;
}

.el-main {
  background-color: #eaedf1;
}
</style>
