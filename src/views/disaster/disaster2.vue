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
const docTitle = ref('四川筠连山体滑坡应急监测评估');
const docSubtitle = ref('');
const docMeta = ref('2025年2月10日');

// HTML 内容
const htmlContent = ref(`
  <p>2025年2月8日11时50分许，四川省宜宾市筠连县沐爱镇金坪村发生山体滑坡，造成了重大人员伤亡和财产损失。灾害发生后，应急管理部国家减灾中心紧急启动重大灾害应急无人机合作机制，就近调拨了4支队伍共11人携带15架无人机，可见光、Lidar、热红外等载荷以及照明、喊话、抛投、卫星通讯等设备赶赴灾区开展无人机应急监测。</p>

  <h2>应急监测工作</h2>

  <p>飞行队于2月8日当天16时30分抵达现场后立刻展开飞行，至2月9日飞行队共飞行18架次，巡查8.3公里，监测面积约5平方公里，拍摄全景图10幅、视频28段、相片20余张，高效支撑了中心对灾区滑坡碎屑流、房屋冲毁和掩埋、二次滑坡风险等情况的分析研判，并配合消防队伍人员搜救开展夜间系留照明工作。</p>

  <div class="image-container">
    <img src="/images/disaster/disaster2-1.png" alt="滑坡现场全景" />
  </div>

  <div class="image-row" style="display: flex; justify-content: center">
    <div class="image-container">
      <img src="/images/disaster/disaster2-2.png" alt="搜救现场" />
    </div>
    <div class="image-container">
      <img src="/images/disaster/disaster2-3.png" alt="无人机操作" />
    </div>
  </div>

  <div class="image-container">
    <img src="/images/disaster/disaster2-4.png" alt="夜间照明作业" />
  </div>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}
</style>