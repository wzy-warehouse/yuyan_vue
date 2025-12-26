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
const docTitle = ref('2025年考核和增补工作圆满完成');
const docSubtitle = ref('重大灾害无人机应急合作机制');
const docMeta = ref('3月7日');

// HTML 内容
const htmlContent = ref(`
  <p><strong>使命在肩，责任如山。</strong>为充分发挥专业化、多元化、点多面广的社会无人机力量，全面提升重大灾害风险和应急处置工作效能，2024年底至2025年初，应急管理部国家减灾中心携手"重大灾害无人机应急合作机制"成员单位，联合大疆应急联盟、飞马等行业无人机单位，开展了机制到期单位考核和合作单位增补工作，并于2025年2月28日-3月4日对合格单位进行了公示。</p>

  <p>经过本轮考核和增补，2025年度，机制合作单位数量已突破200家，全国无人机应急网络节点进一步织密，应急响应效率将得到大幅提升。</p>

  <p><strong>感谢每一位成员的辛勤付出，也热烈欢迎新成员的加入！</strong>让我们携手聚力，共同为国家防灾减灾救灾事业贡献力量，守护人民生命财产安全，铸就坚不可摧的应急防线。</p>

  <p><strong>未来已来，我们并肩前行！</strong></p>

  <div class="image-container">
    <img src="/images/dynamic/dynamic2-1.png" alt="考核增补工作图表" />
    <div class="image-caption">机制单位考核与增补工作图示</div>
  </div>

  <div class="image-container">
    <img src="/images/dynamic/dynamic2-2.png" alt="机制网络分布图" />
    <div class="image-caption">全国无人机应急网络分布图</div>
  </div>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}
</style>