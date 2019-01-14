<template>
  <div class="business">
    <div class="explain">
      代理招商说明
    </div>
    <el-collapse>
      <el-collapse-item title="一、项目能为代理商带来的价值" name="1" class="title">
        <div>1、经济效益</div>
        <div>一个三人团队的代理商在一个地级代理区一年的收入预算为182万元（见本说明第九条的详细计算）。</div>
        <div>一个代理商建立一个十人团队，可以选择三个代理区进行代理合作，这样，其年度预算收入为546万元。</div>
        <div>包含用户推广代理酬金、产品配件代销收益、平台广告招揽代理酬金。</div>
        <div>2、市场新机遇</div>
        <div>随着项目的推广，一个有着精准专业性，且规模巨大的用户群体即将形成，可以支撑系统良好的广告价值，附带的电商平台可以形成大量的高效线上交易。</div>
        <div>代理商可以在电商商户入住招揽中形成代理收益。</div>
        <div>为代理商发展新型服务业务提供良好的市场先机。</div>
      </el-collapse-item>
      <el-collapse-item title="二、代理商合作政策" name="2" class="title">
        <div>1、代理商酬金线上按月结算，线下按月支付</div>
        <div>2、代理商月度代理费（酬金）=代理商所推广的用户第一年实际逐月缴费额的30%+代理商当月招揽广告业务逐月收入的50%+电商平台入住商户开发提成收入</div>
        <div>3、代理商分销产品配件每件允许加价5-10元（运营方不接受1000件以下的采购订单）</div>
        <div>4、为代理商的全部相关员工提供相关培训</div>
        <div>5、代理商的保证金</div>
        <div>一个代理商缴纳的保证金为其年度预算收入的3%左右。</div>
        <div>代理商的年度预算收入=代理商年度终端账户开发工作指标*250元*0.3+代理商年度终端账户开发工作指标*5元（产品配件代销收益）+代理区年度招揽广告业务工作指标*0.5+代理区电商平台入住商户开发年度提成收入</div>
        <div>6、代理商保证金的使用</div>
        <div>保证金用于保证代理商的合规合法经营。违规违法经营，或未能完成工作指标的20%的，扣除部分保证金，直至终止代理权，解除合同。代理商的经营行为造成较大经济损失和较大负面社会影响，保证金不足以偿付损失的，代理商另行赔付。</div>
        <div>具体内容见《远信市场开发代理合同》。</div>
      </el-collapse-item>
      <el-collapse-item title="三、代理商准入条件" name="3" class="title">
        <div>1、信誉良好的法人实体，或信誉良好的拟创业个人。</div>
        <div>2、认同项目的市场前景和社会价值，愿意成为项目的一个代理商。</div>
        <div>3、愿意接受按本说明第十条计算出的或更高的年度工作指标。</div>
        <div>4、愿意接受按本说明第二条第5款计算出的或更高的保证金额度。</div>
        <div>5、愿意接受《远信市场开发代理合同》的全部条款。</div>
      </el-collapse-item>
      <el-collapse-item title="四、代理商业绩管理办法" name="4" class="title">
        <div>1、未完成月度工作指标的10%、或连续两个月未能完成月度工作指标的15%、或未完成季度工作指标的20%的，扣除保证金的20%，终止代理权，区域内代理权重新招商。</div>
        <div>2、完成年度工作指标、或未完成年度工作指标但没有代理竞争人出现的，可以续签次年代理合同。</div>
        <div>3、跨区域开展市场推广的，该部分业绩不纳入业绩统计和代理费结算，且每跨区域推广一个用户扣除保证金1000元。</div>
      </el-collapse-item>
      <el-collapse-item title="五、项目用户市场数据分析" name="5" class="title">
        <el-table :data="tableData" style="width: 100%">
          <el-table-column prop="date" label="行业" width="180">
          </el-table-column>
          <el-table-column prop="name" label="商户数" width="180">
          </el-table-column>
          <el-table-column prop="address" label="用工（终端）数">
          </el-table-column>
        </el-table>
        <div>
          <p style="font-size:16px">计划用三年时间覆盖50%，用工（终端）数3000万*0.5=1500万个，平均每年新增500万个终端账户。</p>
        </div>
      </el-collapse-item>
      <el-collapse-item title="六、代理商分布规划" name="6" class="title">
        <div>全国有333个地级行政单位（地级市、地区、自治州、盟）。</div>
        <div>规划设置333个代理商代理区域。</div>
        <div>一个代理商可选择多个代理区域合作。</div>
      </el-collapse-item>
      <el-collapse-item title="七、代理商年度终端账户开发工作平均指标计算" name="7" class="title">
        <div>代理商年度终端账户开发工作平均指标=项目用户发展年度总目标/代理区规划数量=500万个/333=1.5万个</div>
        <div>年度目标：1.5万；季度目标：3750；月度目标：1250</div>
        <div>相当于拥有3名推广员的代理商每人每工作日成功推广一个有20名用工的用户。</div>
      </el-collapse-item>
      <el-collapse-item title="八、代理商年度招揽广告业务平均指标设定" name="8" class="title">
        <div>中国2017年GDP总量82.71万亿元，333个代理区域平均GDP为2480亿元。</div>
        <div>每1000亿GDP设定50万元的招揽广告业务指标。</div>
        <div>每个代理商招揽广告业务平均指标为2.48*50万元=124万元。</div>
      </el-collapse-item>
      <el-collapse-item title="九、代理商的平均年度收入预算" name="9" class="title">
        <div>代理商的年度预算收入=代理商年度终端账户开发工作指标*250元*0.3+代理商年度终端账户开发工作指标*5元（产品配件代销收益）+</div>
        <div>代理区年度招揽广告业务工作指标*0.5+代理区电商平台入住商户开发年度提成收入=1.5万*250元*0.3+1.5万*5元+124万元*0.5+0=182万元</div>
        <div>代理商如果组建一个10人团队，可以选择三个代理区进行合作，其理论预算收入为：182*3=546万元</div>
      </el-collapse-item>
      <el-collapse-item title="十、代理商具体年度工作指标的计算规则" name="10" class="title">
        <div>1、代理商终端账户开发年度工作指标=1.5万个*代理区域上年GDP*333/上年全国GDP</div>
        <div>2、代理商广告招揽年度工作指标=50万元*代理区域上年GDP/1000亿元 （项目推广第一年该指标减半计算）</div>
        <div>3、代理商电商平台入住商户开发年度指标，根据项目推广情况适时发布 （项目推广第一年该指标不考核）</div>
      </el-collapse-item>
      <el-collapse-item title="十一、项目推广的市场支持政策" name="11" class="title">
        <div>1、免费试用：用户上线第一个月可安排15个以内的终端上线免费试用。</div>
        <div>2、微用户永久免费：用户的终端账户不多于三个可一直免费使用。</div>
        <div>3、悬赏征集项目缺陷活动：用户发现的项目应用缺陷被运营方接受的给与一定的奖励。</div>
        <div>4、代理权保留特惠：首期签约的前10个代理商可在其代理区周边保留1-2个代理区的优先签约权。</div>
      </el-collapse-item>
      <el-collapse-item title="十二、招商中心" name="12" class="title">
        <div>地址：上海市宝山区陆翔路111弄1号楼1215-1216室</div>
        <div>热线电话：021-66788812</div>
        <div>联系人：陈先生</div>
      </el-collapse-item>
    </el-collapse>
  </div>
</template>

<script>
export default {
  name: "Business",
  data() {
    return {
      tableData: [
        {
          date: "酒店保安保洁",
          name: "26万",
          address: "400万"
        },
        {
          date: "物业保安保洁",
          name: "12万",
          address: "800万"
        },
        {
          date: "小型装潢施工",
          name: "10万",
          address: "200万"
        },
        {
          date: "乡村保安保洁",
          name: "70万",
          address: "400万"
        },
        {
          date: "工厂保安保洁",
          name: "100万",
          address: "1000万"
        },
        {
          date: "基础设施巡检",
          name: "5万",
          address: "100万"
        },
        {
          date: "治安管理巡逻",
          name: "5万",
          address: "100万"
        },
        {
          date: "合计",
          name: "228万",
          address: "3000万"
        }
      ]
    };
  },
  methods: {},
  mounted() {}
};
</script>

<style scoped>
.business {
  width: 100%;
  height: 100%;
  padding: 0 20%;
}

.title div {
  text-align: left;
  padding-left: 20%;
}

.explain{
    font-size: 32px;
    padding:30px;
}
</style>

