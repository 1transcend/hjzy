<template>
    <div class="footer">
      <div class="container">
        <div class="footer-text">
          <a href title="关于我们">关于我们</a>
          <a href title="文库协议">文库协议</a>
          <a href title="意见反馈">意见反馈</a>
          <a href title="联系我们">联系我们</a>
        </div>
        <div class="footer-text">
          IT文库(wenku.it)  ©2017
        </div>
      </div>
    </div>
  <!-- 底部结束 -->
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style>
.footer {
  height: 79px;
  background-color: #666;
  padding: 40px;
}

.footer .container{
    width: 1100px;
    padding:0 15px;
}

.footer .footer-text {
  /* height: 80px; */
  font-size: 13px;
  padding-right:15px;
  padding-left:15px;
  text-align: center;
  color: #fff;
}

.footer .footer-text a {
  margin: 0 8px;
  display: inline-block;
  color: #fff;
  height: 26px;
}
</style>
