<template>
  <div class="introduce">
    <div class="companyIntroduce">
      <div class="introduceContent">
        <div class="gsln">
          <span style="font-size:32px;">公司理念：</span>
        </div>
        <div class="gsnr">
          <span>智创未来，助力发展，服务大众，成就自我。</span>
        </div>
        <div class="gsnr2">
          <br>
          <br>上海见慧企业发展有限公司成立于2016年5月，致力于生产过程智能化和生产管理互联网化的研究和市场发展工作。
          <br>
          <br>2018年7月，公司研究团队瞄准单人分散作业相关行业存在的管理难题，开展了大量研究和产品开发工作，打造了工业互联网概念产品“远信”。
        </div>
      </div>
    </div>
    <div class="aboutCompany">
      <div style="height:35px;font-size:24px;">我们的服务</div>
      <div style="height:30px;color:grey">our services</div>
      <div>
        <img src="../assets/circle.png" alt>
      </div>
      <div style="font-size:24px;color:red;padding:10px 0">
        远程协助 + 远程会议 + 远程监督 + 实时对讲 =
        <span
          style="font-size:36px;color:black;font-weight:600;border-bottom:5px solid #959595"
        >远 信</span>
      </div>
      <div style="padding:5px 20%">
        <el-collapse>
          <el-collapse-item title="一、	产品定位" name="1">
            <div>基于移动终端和智能云端的对单人分散作业的远程透明化管理工具</div>
            <div>解决单人分散作业远程监督和沟通问题的智能化互联网化辅助工具</div>
          </el-collapse-item>
          <el-collapse-item title="二、	能够解决的问题" name="2">
            <div>酒店保安保洁、物业保安保洁、小型装潢施工、乡村保安保洁、基础设施巡检、治安管</div>
            <div>理巡逻等工作中的作业者多为单人分散作业，管理者进行监管和指导的效率极低、成本极</div>
            <div>高，作业者存在谎报作业、低效作业、停滞作业、冒名顶替作业、不按标准作业的可能，形</div>
            <div>成了一定的社会问题。</div>
            <div>远信为管理者提供单人作业的远程透明化管理和协助工具，可以使作业者回归到敬业负</div>
            <div>责的工作状态，可以随时指导作业者解决工作遇到的问题，为单人作业的工作数量和工作质</div>
            <div>量达到管理者的要求提供可靠的管理工具。</div>
          </el-collapse-item>
          <el-collapse-item title="三、	解决问题的方案" name="3">
            <div>以单人作业者持有的移动通讯终端设备为基本载体，利用云端服务技术，为管理者提供</div>
            <div>不影响作业进程的远程监督和远程沟通解决方案。</div>
            <div>远信的远程管理和沟通主要包括“千里眼”、“顺风耳”、“会议室”、“远控手”四个组件。</div>
            <div>借助这四个组件，管理者对分散在多处远端的单人作业能看到，能听到，能说到，保证能做</div>
            <div>到。</div>
            <div>千里眼：即远程监督。实时采集作业者工作现场数据供管理者对其工作进行监督。</div>
            <div>顺风耳：即数字式无线对讲机。</div>
            <div>会议室：即数字电话会议系统。</div>
            <div>远控手：即远程协助作业。以基于作业者现场视频的电话会议，由作业者实施管理者的</div>
            <div>作业构想和对作业者进行作业指导及培训的工作模式。</div>
          </el-collapse-item>
          <el-collapse-item title="四、	能够为用户带来的价值" name="4">
            <div>1、 提高服务质量</div>
            <div>通过“远信” 的辅助管理，管理者能够对员工作业实施有效的监督、指导和管控，能</div>
            <div>够保证员工按照用户对其客户的服务承诺实施作业，提高用户的市场信誉。</div>
            <div>胖东来解决这个问题的主要方法是，给保安、保洁员增加一倍的工资，大约相当于每人</div>
            <div>每天增加开支50-100元。</div>
            <div>这对于一个100人左右的团队来说，每年需要增加开支125-250万元。</div>
            <div>2、 大幅度降低管理成本</div>
            <div>通过“远信” 的辅助管理，能几倍甚至几十倍地提高工作监督和沟通的效率，可以大</div>
            <div>幅度减少用户配置的管理监督人员，大幅度降低用户的管理成本。</div>
            <div>一个拥有10个班组总人数100人左右的作业团队，需要配置领班、巡检、队长等管理人</div>
            <div>员10-15名，使用远信辅助管理后，仅保留2名管理人员即可，可减少管理开支约每年50万元，</div>
            <div>每月4万多元，相当于每人每天减少开支20元。</div>
            <div>一般还要一次性配置对讲机100部，使用远信辅助管理后可以完全省去，每部对讲机按</div>
            <div>400元计算，可以为用户节省4万元的投资款。按折旧和普通的投资收益算，相当于每人每天</div>
            <div>减少开支4元。</div>
          </el-collapse-item>
          <el-collapse-item title="五、	增值服务（配套专业电商平台）" name="5">
            <div>系统附带面向系统用户及其用工的电商交易平台，能够为系统用户及其供应商提供精准</div>
            <div>专业的广告和线上交易服务。</div>
          </el-collapse-item>
          <el-collapse-item title="六、	服务计费方案" name="6">
            <div>每人每上线工作1天收服务费1元</div>
            <div>按每年每人工作250天计算，用户每人每年开支250元</div>
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
  </div>
</template>

<script>
export default {
  name: "Introduce",
  data() {
    return {
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
      ]
    };
  },
  methods: {},
  mounted() {}
};
</script>

<style scoped>
.introduce {
  width: 100%;
  height: 100%;
}
.companyIntroduce {
  position: relative;
  height: 26%;
  background: #e8e8e8;
  color: #d81b43;
  font-family: "YouYuan";
  font-size: 14px;
}
.introduceContent {
  position: relative;
  top: 15px;
}
.gsln {
  position: relative;
  right: 10%;
}
.gsnr {
  position: relative;
  left: 43%;
  bottom: 26px;
  width: 400px;
  font-size: 18px;
}
.gsnr2 {
  position: relative;
  bottom: 30px;
  font-size: 14px;
}
.aboutCompany {
  width: 100%;
  height: 70%;
  padding-bottom: 50px;
}
</style>