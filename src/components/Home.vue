<template>
  <div class="home">
    <el-header height="120px">
      <div class="top">
        <div class="head-left">
          <div class="logo-img">
            <img src="../assets/logo1.png" alt height="120px">
          </div>
          <div class="word">
            <div style="padding:30px 0 0 0;text-align:left">遥可及 远可信</div>
            <div style="padding:10px 0 0 0;text-align:left">远信——实现作业管理的远程化、透明化</div>
          </div>
        </div>
        <div class="head-right">
          <el-menu default-active="1" class="el-menu-demo" mode="horizontal">
            <el-menu-item index="1" class="tag" @click="toShow(1)">首页</el-menu-item>
            <el-menu-item index="2" class="tag" @click="toShow(2)">代理招商说明</el-menu-item>
            <el-menu-item index="3" class="tag" @click="toShow(3)">代理合同文本</el-menu-item>
          </el-menu>
        </div>
      </div>
    </el-header>
    <div class="center">
      <el-carousel :interval="5000" :height="imgHeight">
        <el-carousel-item v-for="item in imgList" :key="item.id">
          <img ref="imgHeight" :src="item.idView" width="100%" />
        </el-carousel-item>
      </el-carousel>
    </div>
    <div class="content">
      <component :is="isShow"></component>
    </div>
    <div class="bottom">
      <div class="bottom-left">
        <div class="bottom-companyname">
          <span />远信
        </div>
        <div class="bottom-companynotice">
          <span />遥可及，远可信
        </div>
      </div>
      <div class="bottom-center">
        <div class="center-content">
          <img src="../assets/tel.png" alt>
          <span style="top:10px;">+86 56563252</span>
        </div>
      </div>
      <div class="bottom-right">
        <div class="bottom-company-name">
          <span />上海见慧企业发展有限公司
        </div>
        <div class="bottom-company-notice" style="width: 200px;margin:0;">
          <p>智创未来，助力发展</p>
          <p>服务大众，成就自我</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Business from "./Business";
import Contract from "./Contract";
import Introduce from "./Introduce";

export default {
  name: "Home",
  components: {
    Introduce,
    Business,
    Contract
  },
  data() {
    return {
      imgList: [
        { id: 0, idView: require("../assets/lunbo1.png") },
        { id: 1, idView: require("../assets/lunbo2.png") }
      ],
      screenWidth: document.documentElement.clientWidth,
      imgHeight: '',
      isShow: Introduce
    };
  },
  methods: {
    load(){
      setTimeout(() => {
        this.imgHeight = Number(this.$refs.imgHeight[0].height) + "px"
      }, 100);
    },
    toShow(val) {
      if (val === 1) {
        this.isShow = Introduce;
      } else if (val === 2) {
        this.isShow = Business;
      } else {
        this.isShow = Contract;
      }
    }
  },
  watch: {
    screenWidth: function() {
      this.imgHeight = Number(this.$refs.imgHeight[0].height) + "px"
    }
  },
  mounted() {
    var _this = this
    window.onresize = function() {
      _this.screenWidth = document.documentElement.clientWidth
    }
    this.load()
  }
};
</script>

<style scoped>
.home {
  width: 100%;
  height: 100%;
}

.top {
  width: 100%;
  height: 120px;
  background-color: #ffffff;
}

.center {
  width: 100%;
  height: auto;
  background-color: #e8e8e8;
}

.content {
  width: 100%;
  height: auto;
}

.bottom {
  width: 100%;
  height: 150px;
  background-color: #1f2025;
}

.head-left {
  float: left;
  padding-left: 80px;
  width: 50%;
  height: 120px;
}

.head-right {
  float: right;
  width: 50%;
  height: 120px;
  padding: 35px 0 0 35px;
}

.logo-img {
  float: left;
  width: 170px;
}

.word {
  height: 120px;
  font-size: 20px;
}

.tag {
  font-size: 20px;
  padding: 0 45px;
}
</style>

<style>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

.bottom-left {
  width: 25%;
  height: 150px;
  float: left;
}
.bottom-center {
  width: 40%;
  height: 150px;
  float: left;
}
.bottom-right {
  width: 33%;
  height: 150px;
  float: right;
}
.bottom-companyname {
  position: relative;
  top: 30px;
  right: 60px;
  color: #b3b3b3;
  font-size: 48px;
  font-family: "YouYuan";
}
.bottom-companynotice {
  position: relative;
  top: 30px;
  left: 80px;
  color: #b3b3b3;
  font-size: 16px;
  font-family: "YouYuan";
}
.center-content {
  position: relative;
  top: 30px;
  color: #b3b3b3;
  font-size: 36px;
  font-family: "YaHei UI";
}
.bottom-company-name {
  position: relative;
  top: 20px;
  right: 60px;
  color: #b3b3b3;
  font-size: 36px;
  font-family: "YouYuan";
}
.bottom-company-notice {
  position: relative;
  top: 30px;
  left: 180px;
  color: #b3b3b3;
  font-size: 12px;
  font-family: "YouYuan";
}

.el-menu-demo {
  width: 555px;
}
</style>

