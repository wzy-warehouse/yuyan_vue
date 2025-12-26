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
const docTitle = ref('灾害应急：云南福贡县亚目水电站滑坡应急监测');
const docSubtitle = ref('');
const docMeta = ref('3月18日，云南怒江');

// HTML 内容
const htmlContent = ref(`
  <p>3月18日4时云南省怒江州福贡县鹿马登乡亚坪村拉甲村民小组发生山体滑坡。灾害发生后，国家减灾中心紧急启动重大灾害无人机应急合作机制，就近调拨1支飞行队携带2架无人机及可见光、倾斜、Lidar等多种类载荷赶赴灾区开展无人机监测与辅助救援。</p>

  <h2>高效响应与精准监测</h2>

  <p>队伍接到指令后立即转场，3小时后抵达灾害现场开展应急监测，获取滑坡及周边0.23平方公里范围内高精度倾斜摄影影像，支撑中心开展灾区滑坡范围、土石方量、房屋损毁情况等的分析研判，并配合消防救援队伍开展现场灾害风险防控工作。</p>

  <div class="image-container">
    <img src="/images/disaster/disaster3-1.png" alt="水电站滑坡全景" />
  </div>

  <div class="image-container">
    <img src="/images/disaster/disaster3-2.png" alt="滑坡体细节" />
  </div>

  <div class="image-container">
    <img src="/images/disaster/disaster3-3.png" alt="救援配合" />
  </div>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}
</style>