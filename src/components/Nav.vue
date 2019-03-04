<template>
  <div class="nav">
    <el-menu
      :default-active="activeIndex"
      class="el-menu-demo"
      mode="horizontal"
      @select="handleSelect"
    >
      <el-menu-item index="1">
        <router-link to="/">首页</router-link>
      </el-menu-item>
      <el-menu-item index="2">
        <router-link to="/list">编程开发</router-link>
      </el-menu-item>
      <el-menu-item index="3">
        <router-link to="/list1">系统运维</router-link>
      </el-menu-item>
      <el-menu-item index="4">
        设计·创作
      </el-menu-item>
      <el-menu-item index="5">
        云计算·大数据
      </el-menu-item>
      <el-menu-item index="6">
        产品·运营·综合
      </el-menu-item>
      <el-menu-item index="7">
        文库开源
      </el-menu-item>
      <el-menu-item index="8" class="el-icon-upload2">
        上传文档
      </el-menu-item>
      <el-menu-item index="9" class="el-icon-service">
        会员中心
      </el-menu-item>
    </el-menu>
  </div>
  <!-- 导航栏结束 -->
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
    },
    name: "Nav"
};
</script>

<style>
.nav {
  margin-bottom: 15px;
  background-color: #34495e;
}

.nav .el-menu-demo {
  width: 1100px;
  height: 53px;
  margin-right: auto;
  margin-left: auto;
  border-bottom: 0px !important;
  background-color: #34495e;
  font-weight: 700;
}

.nav .el-menu-item {
  height: 53px !important;
  font-size: 16px;
  color: #fff !important;
  border: 0px !important;
  padding: 16px 23px;
  text-align: center;
  line-height: 21px !important;
}

.el-menu--horizontal > .el-menu-item:not(.is-disabled):hover {
  background-color: #34495e !important;
  color: #1abc9c !important;
}

.is-active {
  background-color: #1abc9c;
}

.el-menu--horizontal > .el-menu-item:not(.is-disabled):focus {
  background-color: #1abc9c !important;
  color: #fff !important;
}

.nav [class*=" el-icon-"],
[class^="el-icon-"] {
  font-weight: 700 !important;
}
/* 导航栏结束 */
</style>
