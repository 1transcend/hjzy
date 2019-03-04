<template>
  <div id="app">
    <!-- logo组件 -->
    <Logo/>
    <!-- 导航栏组件 -->
    <Nav/>
    <!-- 路由视图 -->
    <router-view></router-view>
    <!-- 底部组件 -->
    <Footer/>
  </div>
</template>

<script>
import Logo from "@/components/Logo";
import Nav from "@/components/Nav";
import Footer from "@/components/Footer";

export default {
  components: {
    Logo,
    Nav,
    Footer
  }
};
</script>

<style>
@import "./assets/css/app.css";
* {
  padding: 0px;
  margin: 0px;
}
body {
  background-color: #f6f6f6;
}
a {
  color: #555;
  cursor: pointer;
  text-decoration: none;
}
img {
  vertical-align: middle;
}
ul,
li {
  list-style: none;
}
</style>