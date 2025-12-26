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
const docTitle = ref('国家减灾中心派员参加2025第九届世界无人机大会');
const docSubtitle = ref('暨UASE无人机展');
const docMeta = ref('5月23日');

// HTML 内容
const htmlContent = ref(`
  <p>5月23日至25日，国家减灾中心派员参加第九届世界无人机大会暨国际低空经济与无人系统博览会（以下简称"UASE无人机展"）。本届大会在广东深圳会展中心举办，以"步入低空经济新时代"为主题，设置全体大会和50余场主题论坛，集中展示了全球无人机产业的最新发展成果，吸引超过100个国家和地区的825家相关企业参展、超过10万人次观展。</p>

  <p>UASE无人机展聚焦低空经济产业高质量发展成果，展区覆盖低空智能制造、低空数字交通、eVTOL、人工智能机器人、低空基础设施与管理平台、无人系统全产业链、物流应急无人机等多个前沿领域。国家减灾中心根据航空业务发展需要，充分调研多家企业，深入了解无人机在应急救援、物流运输、电力巡检、森林防护、遥感测绘等多个场景的创新应用成果。</p>

  <div class="image-container">
    <img src="/images/dynamic/dynamic5-1.png" alt="无人机大会现场" />
    <div class="image-caption">第九届世界无人机大会现场</div>
  </div>

  <p>在平行论坛会场上，主题分论坛从产业政策、技术市场、场景应用、综合发展等层面出发，涵盖无人机应急救援、低空经济与消防无人机生态建设、无人机遥感测绘技术应用等多个领域。国家减灾中心参与多场论坛会议，其中，无人机应急救援高峰论坛以"使命必达·安邦惠民"为主题，深入探讨了无人机在应急管理领域的应用与发展。</p>

  <p>与会专家强调，加强航空应急救援能力建设不仅能为低空经济发展注入新动能，又是增强应急管理体系效能的关键手段。论坛指出，当前亟需加快应急救援平台建设、提升政企协同能力、推动装备研发创新，以加强完善现代应急管理体系建设。</p>

  <div class="image-container">
    <img src="/images/dynamic/dynamic5-2.png" alt="无人机应急救援论坛" />
    <div class="image-caption">无人机应急救援高峰论坛现场</div>
  </div>

  <p>下一步，国家减灾中心将继续依托低空经济产业发展优势，面向应急管理和防灾减灾救灾事业发展需要，积极融入"大安全、大应急"框架，进一步扩大"雨燕应急·重大灾害无人机应急合作机制"影响力，强化提升无人机监测快速响应、精准识别、全面覆盖和专业处置能力，加快构建"天-空-地-人"一体化监测预警体系中"空基"核心业务的体系化、智能化、标准化发展。</p>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}
</style>