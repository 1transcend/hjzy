<template>
  <div class="conter">
    <div class="container">
      <el-col :span="6">
        <a href="javascript:;" title="IT文库(wenku.it)">
          <img src="@/assets/images/logo.png" alt="IT文库(wenku.it)">
        </a>
      </el-col>
    </div>
  </div>
  <!-- logo结束 -->
</template>

<script>
export default {
  name: "Logo"
};
</script>

<style>
.conter {
  padding: 0 15px;
  margin-right: auto;
  margin-left: auto;
  background-color: #fff;
}
.container {
  padding: 0px;
  margin-right: auto;
  margin-left: auto;
  width: 1100px;
  height: 80px;
}
.container .el-col-6 {
  width: 50%;
}
.container img {
  margin: 10px 0px;
  height: 60px;
}
</style>
