<template>
    <div class="product">
        <div class="top">
            <el-row>
                <el-col :span="1">
                    <div>&nbsp;</div>
                </el-col>
                <el-col :span="8">
                    <div style="height:45px;border-bottom:solid 2px black">&nbsp;</div>
                </el-col>
                <el-col :span="6">
                    <div :class="[isCorrectSize ? classObject.programme : classObject.programmea]">"远信"&nbsp;&nbsp;&nbsp;&nbsp;解决问题的方案</div>
                </el-col>
                <el-col :span="8">
                    <div style="height:45px;border-bottom:solid 2px black">&nbsp;</div>
                </el-col>
                <el-col :span="1">
                    <div>&nbsp;</div>
                </el-col>
            </el-row>
        </div>
        <div class="center">
            <div class="picture" v-for="item in pictureList" :key="item.id">
                <img :src="item.imgUrl" alt="" width="400px" height="260px">
                <div style="width:350px;margin:auto;padding:10px 0 0 0">
                    {{item.imgMessage}}
                </div>
            </div>
        </div>
        <div style="padding:5px 20%">
            <el-collapse>
                <el-collapse-item title="一、	产品定位" name="1" class="title">
                    <div>1、基于移动终端和智能云端的对单人分散作业的远程透明化管理工具</div>
                    <div>2、解决单人分散作业远程监督和沟通问题的智能化互联网化辅助工具</div>
                </el-collapse-item>
                <el-collapse-item title="二、	能够解决的问题" name="2" class="title">
                    <div>1、酒店保安保洁、物业保安保洁、小型装潢施工、乡村保安保洁、基础设施巡检、治安管理巡逻等工作中的作业者多为单人分散作业，管理者进行监管和指导的效率极低、成本极高，作业者存在谎报作业、低效作业、停滞作业、冒名顶替作业、不按标准作业的可能，形成了一定的社会问题。</div>
                    <div>2.远信为管理者提供单人作业的远程透明化管理和协助工具，可以使作业者回归到敬业负责的工作状态，可以随时指导作业者解决工作遇到的问题，为单人作业的工作数量和工作质量达到管理者的要求提供可靠的管理工具。</div>
                </el-collapse-item>
                <el-collapse-item title="三、	解决问题的方案" name="3" class="title">
                    <div>1、以单人作业者持有的移动通讯终端设备为基本载体，利用云端服务技术，为管理者提供不影响作业进程的远程监督和远程沟通解决方案。</div>
                    <div>2、远信的远程管理和沟通主要包括“千里眼”、“顺风耳”、“会议室”、“远控手”四个组件。借助这四个组件，管理者对分散在多处远端的单人作业能看到，能听到，能说到，保证能做到。</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;千里眼：即远程监督。实时采集作业者工作现场数据供管理者对其工作进行监督。</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;顺风耳：即数字式无线对讲机。</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;会议室：即数字电话会议系统。</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;远控手：即远程协助作业。以基于作业者现场视频的电话会议，由作业者实施管理者的作业构想和对作业者进行作业指导及培训的工作模式。</div>
                </el-collapse-item>
                <el-collapse-item title="四、	能够为用户带来的价值" name="4" class="title">
                    <div>1、 提高服务质量</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;通过“远信” 的辅助管理，管理者能够对员工作业实施有效的监督、指导和管控，能够保证员工按照用户对其客户的服务承诺实施作业，提高用户的市场信誉。</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;胖东来解决这个问题的主要方法是，给保安、保洁员增加一倍的工资，大约相当于每人每天增加开支50-100元。</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这对于一个100人左右的团队来说，每年需要增加开支125-250万元。</div>
                    <div>2、 大幅度降低管理成本</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;通过“远信” 的辅助管理，能几倍甚至几十倍地提高工作监督和沟通的效率，可以大幅度减少用户配置的管理监督人员，大幅度降低用户的管理成本。</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;一个拥有10个班组总人数100人左右的作业团队，需要配置领班、巡检、队长等管理人员10-15名，使用远信辅助管理后，仅保留2名管理人员即可，可减少管理开支约每年50万元，每月4万多元，相当于每人每天减少开支20元。</div>
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;一般还要一次性配置对讲机100部，使用远信辅助管理后可以完全省去，每部对讲机按400元计算，可以为用户节省4万元的投资款。按折旧和普通的投资收益算，相当于每人每天减少开支4元。</div>
                </el-collapse-item>
                <el-collapse-item title="五、	增值服务（配套专业电商平台）" name="5" class="title">
                    <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;系统附带面向系统用户及其用工的电商交易平台，能够为系统用户及其供应商提供精准专业的广告和线上交易服务。</div>
                </el-collapse-item>
                <el-collapse-item title="六、	服务计费方案" name="6" class="title">
                    <div>1、每人每上线工作1天收服务费1元</div>
                    <div>2、按每年每人工作250天计算，用户每人每年开支250元</div>
                    <div>具体如下表：</div>
                    <el-table :data="tableData" style="width: 100%">
                        <el-table-column prop="objname" label="方案名称" width="80"></el-table-column>
                        <el-table-column prop="money" label="计费收费办法"></el-table-column>
                        <el-table-column prop="admin" label="管理员" width="80"></el-table-column>
                        <el-table-column prop="leader" label="队长岗" width="80"></el-table-column>
                        <el-table-column prop="groupper" label="队员岗" width="80"></el-table-column>
                    </el-table>
                </el-collapse-item>
            </el-collapse>
        </div>
    </div>
</template>

<script>
export default {
    name: "Product",
    data() {
        return {
            pictureList: [
                {
                    imgUrl: require("../assets/picture1.png"),
                    imgMessage: "劳作者持有的移动通讯终端设备"
                },
                {
                    imgUrl: require("../assets/picture2.png"),
                    imgMessage:
                        "别针式指环挂扣，使沟通的设备和体系不影响劳作者的作业过程"
                },
                {
                    imgUrl: require("../assets/picture3.png"),
                    imgMessage:
                        "终端app自动采集劳作图片及其他实时信息，并自动上传云端提供监督依据"
                },
                {
                    imgUrl: require("../assets/picture4.png"),
                    imgMessage: "基于终端设备的远程协助功能"
                },
                {
                    imgUrl: require("../assets/picture5.png"),
                    imgMessage: "电话会议系统"
                },
                {
                    imgUrl: require("../assets/picture6.png"),
                    imgMessage: "实时的通讯与交流"
                }
            ],
            tableData: [
                {
                    objname: "月结方案",
                    money:
                        " 月缴费额＝a元×当月日历天数＋b元×该用户员工当月使用的人次数（每人每日最多计1次） 初始值：a=1，b=1 次月15日内缴费，逾期按每日3‰计收滞纳金",
                    admin: "1",
                    leader: "任意",
                    groupper: "任意"
                },
                {
                    objname: "试用方案",
                    money: "一个月内免费",
                    admin: "1",
                    leader: "1",
                    groupper: "≦15"
                },
                {
                    objname: "免费方案",
                    money: "免费用至系统不提供服务",
                    admin: "1",
                    leader: "1",
                    groupper: "≦3"
                }
            ],
            classObject:{
                programme:'programme',
                programmea:'programmea'
            }
        };
    },
    props: ["isCorrectSize"],
    methods: {},
    mounted() {}
};
</script>

<style scoped>
.product {
    width: 100%;
    height: 100%;
}

.top {
    width: 100%;
    height: 100px;
}

.center {
    width: 80%;
    height: auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    align-content: flex-start;
    margin: auto;
}

.picture {
    float: left;
    height: 350px;
    flex-grow: 1;
}

.title div {
    text-align: left;
    padding-left: 20%;
    font-size: 15px;
}

.programme {
    font-size: 32px;
    padding: 20px 0 0 0;
    font-weight: 600;
}

.programmea {
    font-size: 26px;
    padding: 20px 0 0 0;
    font-weight: 600;
}
</style>
