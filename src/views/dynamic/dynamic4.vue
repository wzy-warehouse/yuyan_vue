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
import {ref} from 'vue';
import DocumentTemplate from "@/components/template.vue";

// 使用 ref 定义响应式数据
const docTitle = ref('"雨燕应急"2025首期线上培训圆满完成 684名无人机应急尖兵云端集结');
const docSubtitle = ref('');
const docMeta = ref('4月26日');

// HTML 内容
const htmlContent = ref(`
  <p>4月24日下午，应急管理部国家减灾中心在京组织召开了"雨燕应急"2025首期线上培训，聚焦"重大灾害无人机应急合作机制"，旨在强化机制成员灾害应急应对能力。</p>

  <p>此次培训共有220家机制成员单位的684名联络人和一线飞手线上参会，大疆应急行业负责人耿京乐、北京飞马遥测公司杨建华、河南省防灾减灾中心周永春共3名专家受邀在国家减灾中心现场参会。</p>

  <p>国家减灾中心航空遥感应用部王薇主任、李苓苓和杨坤3名同志分别就机制制度、日常管理和应急响应进行了详细讲解，参培人员和专家围绕机制制度规范、工作执行等关键问题展开了交流。</p>

  <h3>培训成效</h3>

  <p>通过培训，增进了机制成员单位联络人和一线飞手对机制运行和应急管理工作的了解，为机制成员单位平战结合，日常开展能力建设、灾害预警等应急准备工作，和在灾害场景下安全、高效、有序执行应急任务提供了明确指导。</p>

  <div class="image-container">
    <img src="/images/dynamic/dynamic4-1.png" alt="培训会议截屏" />
    <div class="image-caption">培训会议现场截屏</div>
  </div>

  <div class="image-container">
    <img src="/images/dynamic/dynamic4-2.png" alt="线上培训界面" />
    <div class="image-caption">线上培训平台界面</div>
  </div>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}
</style>