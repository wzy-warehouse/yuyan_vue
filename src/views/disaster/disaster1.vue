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
const docTitle = ref('西藏定日6.8级地震应急监测评估');
const docSubtitle = ref('');
const docMeta = ref('2025年1月17日');

// HTML 内容
const htmlContent = ref(`
  <p>2025年1月7日9时05分，西藏日喀则市定日县发生6.8级地震，震源深度10公里，震中位于定日县措果乡。此次地震造成了重大人员伤亡和财产损失。</p>

  <p>地震发生后，应急管理部国家减灾中心紧急启动重大灾害应急无人机合作机制，就近调拨了4家单位组成4支飞行队携带发电机、系留照明、抛投器等设备以及10架无人机，可见光、热红外、Lidar等多种类载荷赴西藏定日县受灾严重区域开展地震应急监测。</p>

  <h3>监测成果</h3>

  <p>飞行队于1月7日当天16时30分抵达现场后立刻展开飞行，至1月9日飞行队共飞行117余架次，获取了定日县长所乡、措果乡、曲洛乡和尼辖乡等4个严重受灾乡镇46个村落二三维数据，高效支撑了中心对灾区房屋损失、道路通行等情况的分析研判。</p>

  <div class="image-row">
    <div class="image-container">
      <img src="/images/disaster/disaster1-1.png" alt/>
    </div>
    <div class="image-container">
      <img src="/images/disaster/disaster1-2.png" alt/>
    </div>
  </div>

  <div class="image-row">
    <div class="image-container">
      <img src="/images/disaster/disaster1-3.png" alt/>
    </div>
    <div class="image-container">
      <img src="/images/disaster/disaster1-4.png" alt/>
    </div>
  </div>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}
</style>