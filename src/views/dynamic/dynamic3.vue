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
const docTitle = ref('聚青年英才之力 筑无人机应急防线');
const docSubtitle = ref('');
const docMeta = ref('3月26日');

// HTML 内容
const htmlContent = ref(`
  <p>自2010年建立 "重大灾害无人机应急合作机制" 以来，该机制在历次重特大自然灾害的防灾减灾救灾工作中发挥了重要的技术支撑作用。应急管理部国家减灾中心航空遥感应用部积极推动"重大灾害无人机应急合作机制"的创新发展，按照"开门办中心"的部署，引入青年专家型志愿者共同参与部门能力建设、技术研发和业务支撑工作。</p>

  <h2>青年专家志愿者招募</h2>

  <p>经过前期调研和广泛征求意见，减灾中心已从省级减灾中心、机制合作单位及公益基金会等征集了10名具备无人机技术、应急管理或遥感应用背景的青年专家志愿者。这些志愿者将被聘任为不取酬外聘专家，他们的加入将为无人机应急合作机制注入新的活力，助力减灾中心在重大自然灾害风险防范和应急救援保障工作中发挥更大作用。</p>

  <p>此次引入青年专家志愿者，不仅是减灾中心提升业务能力的重要举措，还是推动"开门办中心"理念落地的具体实践，同时也助力社会企事业单位履行社会责任、共享创新成果、提升品牌价值、培养复合人才，共同以科技创新守护生命防线，用责任担当诠释企业价值。通过青年专家的参与，减灾中心将进一步优化无人机应急合作机制的运行效率，增强技术研发能力，为重大自然灾害的防范和应急救援提供更加坚实的支撑，共同推动无人机应急合作机制的创新发展，为国家的防灾减灾救灾事业贡献力量。</p>

  <div class="image-container">
    <img src="/images/dynamic/dynamic3-1.png" alt="青年专家志愿者工作照" />
    <div class="image-caption">青年专家志愿者参与机制建设</div>
  </div>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}
</style>