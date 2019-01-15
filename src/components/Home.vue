<template>
    <div class="home">
        <el-header height="120px">
            <div class="top">
                <div class="head-left">
                    <div class="logo-img">
                        <img src="../assets/logo1.png" alt="" height="120px">
                    </div>
                    <div class="word">
                        <div class="catchline" :class="classObject.catchlinea">遥可及 远可信</div>
                        <div class="catchline" :class="classObject.catchlinea">实现作业管理的远程化、透明化</div>
                    </div>
                </div>
                <div class="head-right" :class="classObject.headright">
                    <div :class="[isCorrectSize ? classObject.hrlength.hrlength : classObject.hrlength.hrlengtha]">
                        <el-menu default-active="1" class="el-menu-demo" mode="horizontal">
                            <el-menu-item index="1" :class="classObject.taga" @click="toShow(1)">首页</el-menu-item>
                            <el-menu-item index="2" :class="classObject.taga" @click="toShow(2)">代理招商说明</el-menu-item>
                            <el-menu-item index="3" :class="classObject.taga" @click="toShow(3)">代理合同文本</el-menu-item>
                        </el-menu>
                    </div>
                </div>
            </div>
        </el-header>
        <div class="center">
            <el-carousel :height="imgHeight" arrow="never">
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
                    <img src="../assets/tel.png" alt="" width="30px">
                    <span>+021 56563252</span>
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
                { id: 0, idView: require("../assets/lunbo.png") }
                // { id: 1, idView: require("../assets/lunbo2.png") }
            ],
            screenWidth: document.documentElement.clientWidth,
            imgHeight: "",
            isShow: Introduce,
            isCorrectSize: true,
            classObject: {
                catchlinea: {
                    catchlinea: false
                },
                taga: {
                    tag: true,
                    taga: false
                },
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
            if (document.documentElement.clientWidth < 1201) {
                this.isCorrectSize = false;
                this.classObject.catchlinea.catchlinea = true;
                this.classObject.taga.tag = false;
                this.classObject.taga.taga = true;
                this.classObject.headright.headright = true;
                this.classObject.bcname.bottomcompanyname = false;
                this.classObject.bcname.bcname = true;
                this.classObject.btnotice.bottomcompanynotice = false;
                this.classObject.btnotice.btnotice = true;
            }
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
            this.imgHeight = Number(this.$refs.imgHeight[0].height) + "px";
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
    font-size: 14px;
}

.bottom-left {
    width: 50%;
    /* height: 150px; */
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
    /* height: 150px; */
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
}

.catchlinea {
    font-size: 14px;
    padding-top: 14px;
}

.hrlength {
    width: 555px;
}

.hrlengtha {
    width: 320px;
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
</style>

