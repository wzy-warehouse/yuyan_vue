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
const docTitle = ref('"重大灾害无人机应急合作机制"业务交流和技术研讨会');
const docSubtitle = ref('在哈尔滨召开');
const docMeta = ref('1月9日，哈尔滨');

// HTML 内容
const htmlContent = ref(`
  <p>1月9日，"重大灾害无人机应急合作机制"业务交流和技术研讨会在黑龙江省哈尔滨市召开。黑龙江省应急管理厅副厅长闫永军、黑龙江地质矿产局总工程师孙德忠、应急管理部风险监测和火灾综合防治司副司长王成磊、应急管理部地震和地质灾害救援司地质灾害防治指导处二级调研员刘秋强、国家消防救援局高级工程师滕波、应急管理部防汛抗旱司三级调研员汤中倩、应急管理部国家减灾中心副主任张学权参加会议并致辞。</p>

  <h2>会议主要内容</h2>

  <p>会议以习近平新时代中国特色社会主义思想为指导，深入学习贯彻党的二十大和二十届二中、三中全会精神，认真贯彻落实全国应急管理工作会议精神，全面分析"重大灾害无人机应急合作机制"的作用发挥、存在不足和下步工作重点，进一步强化提升无人机监测"快速、精准、全面、专业"能力，更好地为重大灾害指挥决策和救援救灾提供支撑，更深入地服务于各地应急管理系统和相关行业单位。</p>

  <h3>专家报告</h3>

  <p>会上，成都理工大学、应急管理部北方航空护林总站的专家围绕地质灾害航空遥感调查关键技术和无人系统在森林火灾监测预警的实战应用做主旨报告，国家减灾中心航空遥感应用部主任王薇介绍了"重大灾害无人机应急合作机制"相关情况，14家省级单位和6个机制合作单位代表围绕航空应急监测工作业务需求与无人机应急经验作了业务交流和经验分享、提出工作建议。</p>

  <h3>主办协办单位</h3>

  <p>会议由应急管理部国家减灾中心主办，黑龙江省减灾中心、黑龙江省地质矿产局、黑龙江省精臻科技发展有限公司协办，来自16个省（自治区、直辖市）应急管理相关部门负责人和38家机制合作单位140余人参加会议。</p>

  <div class="image-container">
    <img src="/images/dynamic1.jpg" alt="会议现场" />
    <div class="image-caption">会议现场照片</div>
  </div>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}
</style>
