<template>
  <div id="app">
    <div class="conter">
      <div class="container">
        <el-col :span="6">
          <a href="javascript:;" title="IT文库(wenku.it)">
            <img src="./assets/images/logo.png" alt="IT文库(wenku.it)">
          </a>
        </el-col>
      </div>     
    </div>
    <!-- logo结束 -->
    
    <div class="nav">
      <el-menu  :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
        <el-menu-item index="1">首页</el-menu-item>
        <el-menu-item index="2">编程开发</el-menu-item>
        <el-menu-item index="3">系统运维</el-menu-item>
        <el-menu-item index="4">设计·创作</el-menu-item>
        <el-menu-item index="5">云计算·大数据</el-menu-item>
        <el-menu-item index="6">产品·运营·综合</el-menu-item>
        <el-menu-item index="7">文库开源</el-menu-item>
        <el-menu-item index="8" class="el-icon-upload2">上传文档</el-menu-item>
        <el-menu-item index="9" class="el-icon-service">会员中心</el-menu-item>
      </el-menu>
    </div>
    <!-- 导航栏结束 -->

    <div class="row">
      <el-col :span="18">
        <div class="block">
          <el-carousel height="316px">
            <el-carousel-item v-for="(v,k) in img" :key="k">
              <img :src="v" alt="">
            </el-carousel-item>
          </el-carousel>
        </div>
      </el-col>
      <!-- 幻灯片结束 -->

      <el-col class="row-right" :span="6">
        <div class="wenku-count">
          <el-col :span="12">
            <div class="help-block">收录文档</div>
            <span class="text">6244</span>
          </el-col>
          <el-col :span="12">
            <div class="help-block">注册用户</div>
            <span class="text">63</span>
          </el-col>
        </div>

        <div class="panel">
          <div class="panel-body">
            <el-form :inline="true" :model="formInline" class="demo-form-inline">
              <el-input v-model="formInline.user" placeholder="用户名"></el-input>
              <el-input v-model="formInline.password" placeholder="请输入登录密码"></el-input>
              <el-form-item>
                <el-button type="primary" @click="onSubmit">登录文库</el-button>
              </el-form-item>
              <div class="help-block">
                <a class="help-left" href="">忘记密码</a>
                <a class="help-right" href="">注册会员</a>
              </div>
            </el-form>
          </div>
        </div>
      </el-col>
    </div>
    <!-- 侧边栏结束 -->

    <div class="container-fluid">
      <div class="containe">
        <el-row :gutter="20">
          <el-col :span="6">
            <div class="h5">编程开发</div>
            <div class="wenku-list">
              <a href="">前端开发</a>
              <a href="">后端开发</a>
              <a href="">移动开发</a>
              <a href="">游戏开发</a>
              <a href="">硬件开发</a>
              <a href="">开发工具</a>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="h5">系统运维</div>
            <div class="wenku-list">
              <a href="">架构</a>
              <a href="">服务器</a>
              <a href="">操作系统</a>
              <a href="">网络/安全</a>
              <a href="">考试认证</a>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="h5">设计·创作</div>
            <div class="wenku-list">
              <a href="">UI设计</a>
              <a href="">平面设计</a>
              <a href="">设计软件</a>
              <a href="">游戏动画</a>
              <a href="">绘画创作</a>
              <a href="">影视后期</a>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="h5">云计算·大数据</div>
            <div class="wenku-list">
              <a href="">云计算</a>
              <a href="">大数据</a>
              <a href="">数据库</a>
              <a href="">云平台</a>
              <a href="">人工智能</a>
            </div>
          </el-col>
        </el-row>
      </div>
    </div>
    <!-- 数据分类结束 -->

    <div class="wenku-item">
      <el-col :span="12">
        <div class="pane">
          <div class="pane-heading">
            <strong>热门推荐</strong>
          </div>
            <div class="pane-body">
              <el-col :span="10">
                <img src="./assets/images/cover-news.png" alt="">
              </el-col>
              <el-col :span="14">
                <ul>
                  <li>
                    <a href="" title="大学英语II期末复习">大学英语II期末复习</a>
                  </li>
                  <li>
                    <a href="" title="七组订餐项目">七组订餐项目</a>
                  </li>
                  <li>
                    <a href="" title="10minutes ToGit">10minutes ToGit</a>
                  </li>
                  <li>
                    <a href="" title="第一套30道题找不到请自行百度">第一套30道题找不到请自行百度</a>
                  </li>
                  <li>
                    <a href="" title="利用Axure制作需求文档">利用Axure制作需求文档</a>
                  </li>
                </ul>
              </el-col>
            </div>            
        </div>       
      </el-col>
      
      <el-col :span="12" class="wenku-mgl">
        <div class="noborder">
          <div class="panel-default">
            <strong>编程开发</strong>
            <a href="" title="编程开发">更多>></a>
          </div>
          <div class="panel-body">
            <el-col :span="10">
              <img src="./assets/images/cover-coding.png" alt="编程开发">
            </el-col>
            <el-col :span="14">
              <ul>
                <li>
                  <a href="" title="10minutes ToGit">10minutes ToGit</a>
                </li>
                <li>
                  <a href="" title="第一套30道题找不到请自行百度">第一套30道题找不到请自行百度</a>
                </li>
                <li>
                  <a href="" title="利用Axure制作需求文档">利用Axure制作需求文档</a>
                </li>
                <li>
                  <a href="" title="CSS命名规则12">CSS命名规则12</a>
                </li>
              </ul>
            </el-col>
          </div>
        </div>
      </el-col>
    </div>

    <div class="wenku-item">
      <el-col :span="12">
        <div class="noborder">
          <div class="panel-default">
            <strong>系统运维</strong>
            <a href="" title="系统运维">更多>></a>
          </div>
          <div class="panel-body">
            <el-col :span="10">
              <img src="./assets/images/cover-opera.png" alt="系统运维">
            </el-col>
          </div>
        </div>
      </el-col>

      <el-col :span="12" class="wenku-mgl">
        <div class="noborder">
          <div class="panel-default">
            <strong>设计·创作</strong>
            <a href="" title="设计·创作">更多>></a>
          </div>
          <div class="panel-body">
            <el-col :span="10">
              <img src="./assets/images/cover-design.png" alt="设计·创作">
            </el-col>
          </div>
        </div>
      </el-col>
    </div>

    <div class="wenku-item">
      <el-col :span="12">
        <div class="noborder">
          <div class="panel-default">
            <strong>云计算·大数据</strong>
            <a href="" title="云计算·大数据">更多>></a>
          </div>
          <div class="panel-body">
            <el-col :span="10">
              <img src="./assets/images/cover-compute.png" alt="云计算·大数据">
            </el-col>
          </div>
        </div>
      </el-col>

      <el-col :span="12" class="wenku-mgl">
        <div class="noborder">
          <div class="panel-default">
            <strong>产品·运营·综合</strong>
            <a href="" title="产品·运营·综合">更多>></a>
          </div>
          <div class="panel-body">
            <el-col :span="10">
              <img src="./assets/images/cover-product.png" alt="产品·运营·综合">
            </el-col>
          </div>
        </div>
      </el-col> 
    </div>
    <!-- 详细分类结束 -->

    <div class="footer">
      <div class="container">
        <div class="footer-text">
          <a href="" title="关于我们">关于我们</a>
          <a href="" title="文库协议">文库协议</a>
          <a href="" title="意见反馈">意见反馈</a>
          <a href="" title="联系我们">联系我们</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import img from "./assets/images/banner1.png";
import img1 from "./assets/images/banner.png";
export default {
  data() {
    return {
      img:{ 
        img,
        img1
      },
      formInline: {
        user: '',
        password: ''
      },
      activeIndex: '1',
      activeIndex2: '1' 
    }
  },
  methods:{
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      },
      onSubmit() {
        console.log('submit!');
      }
    }
}
</script>

<style>
  @import './assets/css/app.css';
  *{
    padding:0px;
    margin:0px;
  }
  body{
    background-color:#f6f6f6;
  }
  a{
    color:#555;
    cursor:pointer;
    text-decoration:none;
  }
  img{
    vertical-align:middle;
  }
  ul,li{
    list-style:none;
  }
</style>