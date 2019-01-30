<template>
    <div class="home">
        <el-header height="120px">
            <div class="top">
                <div class="head-left">
                    <div class="logo-img">
                        <img src="../assets/logo1.png" alt="" height="120px">
                    </div>
                    <div class="word">
                        <div :class="[isCorrectSize ? classObject.catchline : classObject.catchlinea]">遥可及 远可信</div>
                        <div :class="[isCorrectSize ? classObject.catchline : classObject.catchlinea]">实现作业管理的远程化、透明化</div>
                    </div>
                </div>
                <div class="head-right" :class="classObject.headright">
                    <div :class="[isCorrectSize ? classObject.hrlength.hrlength : classObject.hrlength.hrlengtha]">
                        <el-menu default-active="1" class="el-menu-demo" mode="horizontal">
                            <el-menu-item index="1" :class="[isCorrectSize ? classObject.tag : classObject.taga]" @click="toShow(1)">首页</el-menu-item>
                            <el-menu-item index="2" :class="[isCorrectSize ? classObject.tag : classObject.taga]" @click="toShow(2)">产品介绍</el-menu-item>
                            <el-menu-item index="3" :class="[isCorrectSize ? classObject.tag : classObject.taga]" @click="toShow(3)">招商说明</el-menu-item>
                            <el-menu-item index="4" :class="[isCorrectSize ? classObject.tag : classObject.taga]" @click="toShow(4)">联系我们</el-menu-item>
                            <el-menu-item index="5" :class="[isCorrectSize ? classObject.tag : classObject.taga]" @click="toJump()">登录</el-menu-item>
                        </el-menu>
                    </div>
                </div>
            </div>
        </el-header>
        <div class="center">
            <el-carousel :height="imgHeight">
                <el-carousel-item v-for="item in imgList" :key="item.id">
                    <img ref="imgHeight" :src="item.idView" width="100%" />
                </el-carousel-item>
            </el-carousel>
        </div>
        <div class="content">
            <component :is="isShow" :isCorrectSize="isCorrectSize"></component>
        </div>
        <div class="bottom">
            <div class="bottom-left">
                上海见慧企业发展有限公司
            </div>
            <div class="bottom-right">
                <div class="center-content">
                    <!-- <img src="../assets/tel.png" alt="" width="30px">
                    <span>+021 56563252</span> -->
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Business from "./Business";
// import Contract from "./Contract";
import Introduce from "./Introduce";
import Product from "./Product";
import Connection from "./Connection";

export default {
    name: "Home",
    components: {
        Introduce,
        Business,
        // Contract,
        Product,
        Connection
    },
    data() {
        return {
            imgList: [
                { id: 0, idView: require("../assets/lunbo3.png") },
                { id: 1, idView: require("../assets/lunbo2.png") },
                { id: 2, idView: require("../assets/lunbo1.png") }
            ],
            screenWidth: document.documentElement.clientWidth,
            imgHeight: "",
            isShow: Introduce,
            isCorrectSize: true,
            classObject: {
                catchline: "catchline",
                catchlinea: "catchlinea",
                tag: "tag",
                taga: "taga",
                headright: {
                    headright: false
                },
                hrlength: {
                    hrlength: "hrlength",
                    hrlengtha: "hrlengtha"
                },
                bcname: {
                    bottomcompanyname: true,
                    bcname: false
                },
                btnotice: {
                    bottomcompanynotice: true,
                    btnotice: false
                }
            }
        };
    },
    methods: {
        load() {
            setTimeout(() => {
                this.imgHeight = Number(this.$refs.imgHeight[0].height) + "px";
            }, 100);
            if (document.documentElement.clientWidth < 1370) {
                this.isCorrectSize = false;
                this.classObject.headright.headright = true;
                this.classObject.bcname.bottomcompanyname = false;
                this.classObject.bcname.bcname = true;
                this.classObject.btnotice.bottomcompanynotice = false;
                this.classObject.btnotice.btnotice = true;
            }
        },
        toShow(val) {
            switch (val) {
                case 1:
                    this.isShow = Introduce;
                    break;
                case 2:
                    this.isShow = Product;
                    break;
                case 3:
                    this.isShow = Business;
                    break;
                case 4:
                    this.isShow = Connection;
            }
        },
        toJump(){
            window.open("http://eff.xmidware.com/eff/")
        }
    },
    watch: {
        screenWidth: function() {
            this.imgHeight = Number(this.$refs.imgHeight[0].height) + "px";
            if (this.screenWidth < 1370) {
                this.isCorrectSize = false;
            } else if (this.screenWidth > 1370) {
                this.isCorrectSize = true;
            }
        }
    },
    mounted() {
        var _this = this;
        window.onresize = function() {
            _this.screenWidth = document.documentElement.clientWidth;
        };
        this.load();
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
    height: 120px;
    background-color: #1f2025;
}

.head-left {
    float: left;
    padding-left: 70px;
    width: 50%;
    height: 120px;
}

.head-right {
    float: right;
    width: 50%;
    height: 120px;
    padding: 35px 0 0 35px;
}

.headright {
    padding: 30px 0 0 80px !important;
}

.logo-img {
    float: left;
}

.word {
    height: 120px;
    font-size: 20px;
    padding-top: 20px;
}

.tag {
    font-size: 20px;
    padding: 0 45px;
}

.taga {
    font-size: 16px;
}

.bottom-left {
    width: 50%;
    line-height: 120px;
    float: left;
    color: #b3b3b3;
    font-size: 20px;
    font-family: "YaHei UI";
    padding-right: 30px;
    text-align: right;
}
.bottom-right {
    width: 50%;
    line-height: 120px;
    float: right;
    color: #b3b3b3;
    font-size: 20px;
    font-family: "YaHei UI";
    padding-left: 30px;
    text-align: left;
}
.bottom-companyname {
    position: relative;
    top: 30px;
    right: 60px;
    color: #b3b3b3;
    font-size: 28px;
    font-family: "YouYuan";
}
.bottom-companynotice {
    position: relative;
    top: 40px;
    left: 80px;
    color: #b3b3b3;
    font-size: 18px;
    font-family: "YouYuan";
}
.bottomcompanyname {
    position: relative;
    top: 20px;
    right: 60px;
    color: #b3b3b3;
    font-size: 36px;
    font-family: "YouYuan";
}
.bcname {
    position: relative;
    top: 30px;
    right: 30px;
    color: #b3b3b3;
    font-size: 20px;
    font-family: "YouYuan";
}
.bottomcompanynotice {
    position: relative;
    top: 30px;
    left: 180px;
    color: #b3b3b3;
    font-size: 12px;
    font-family: "YouYuan";
}

.btnotice {
    position: relative;
    top: 40px;
    left: 50px;
    color: #b3b3b3;
    font-size: 12px;
    font-family: "YouYuan";
}

.catchline {
    padding: 10px 0 0 0;
    text-align: left;
    font-size: 20px;
}

.catchlinea {
    font-size: 16px;
    text-align: left;
    padding-top: 14px;
}

.hrlength {
    width: 770px;
}

.hrlengtha {
    width: 460px;
}
</style>

