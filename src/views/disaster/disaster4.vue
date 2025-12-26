<template>
  <div class="page-container">
    <DocumentTemplate
        :title="docTitle"
        :subtitle="docSubtitle"
        :meta="docMeta"
        :content="htmlContent"
        :title-align="'center'"
    >
    </DocumentTemplate>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import DocumentTemplate from "@/components/template.vue";

// 使用 ref 定义响应式数据
const docTitle = ref('灾害应急：贵州大方县果瓦乡山体滑坡无人机应急监测');
const docSubtitle = ref('');
const docMeta = ref('5月22日，贵州毕节');

// HTML 内容
const htmlContent = ref(`
  <p>5月22日，贵州省毕节市大方县果瓦乡庆阳村茶林组发生山体滑坡，造成人员被困。灾害发生后，应急管理部国家减灾中心紧急启动雨燕应急·重大灾害无人机应急合作机制，就近调度1支应急监测飞行队携带多架固定翼、多旋翼无人机及可见光、热红外、Lidar等多种类载荷赶赴灾区开展无人机监测与辅助救援。</p>

  <h2>快速响应与监测</h2>

  <p>队伍接到指令2.5小时后抵达灾害现场开展应急监测，获取滑坡及周边27平方公里范围内高精度正射影像与数字高程模型，国家减灾中心据此开展灾区山体滑坡特征、房屋损毁、堆积体堰塞情况、二次灾害风险等分析研判，以及周边存在安全隐患路段、威胁居民区小型滑坡的识别。</p>

  <div class="image-container">
    <img src="/images/disaster/disaster4-1.png" alt="滑坡灾害现场" />
    <div class="image-caption">果瓦乡山体滑坡现场</div>
  </div>

  <div class="image-row" style="display: flex; justify-content: center">
    <div class="image-container">
      <img src="/images/disaster/disaster4-2.png" alt="救援队伍集结" />
      <div class="image-caption">应急队伍快速集结</div>
    </div>
    <div class="image-container">
      <img src="/images/disaster/disaster4-3.png" alt="设备准备" />
      <div class="image-caption">无人机设备准备</div>
    </div>
  </div>

  <div class="image-container">
    <img src="/images/disaster/disaster4-4.png" alt="数据分析模型" />
    <div class="image-caption">滑坡数据分析模型</div>
  </div>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}
</style>