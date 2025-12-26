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
const docTitle = ref('【灾害应急】山东济南市莱芜区大王庄镇山洪无人机应急监测');
const docSubtitle = ref('');
const docMeta = ref('7月22日-23日，山东济南');

// HTML 内容
const htmlContent = ref(`
  <p><strong>受7月22日凌晨强降雨影响，山东省济南市莱芜区发生山洪灾害，造成大王庄镇部分村庄房屋道路受损。</strong>灾害发生后国家减灾中心紧急启动雨燕应急·重大灾害无人机应急合作机制，就近调度<strong>1支</strong>应急监测飞行队携带多架固定翼与多旋翼无人机及可见光载荷赶赴灾区开展灾害监测。</p>

  <h2>监测工作开展</h2>

  <p>22日15时至23日16时，无人机队伍克服了"三断"环境的影响，开展有效飞行10余架次，<strong>完成大王庄镇受灾严重村庄约5.03平方公里高精度无人机正射影像数据获取。</strong>国家减灾中心据此开展灾区房屋、道路受损情况分析研判。</p>

  <div class="image-row">
    <div class="image-container">
      <img src="/images/disaster/disaster5-1.png" alt="无人机起飞现场" />
    </div>
    <div class="image-container">
      <img src="/images/disaster/disaster5-2.png" alt="设备调试" />
    </div>
  </div>

  <div class="image-container">
    <img src="/images/disaster/disaster5-3.png" alt="灾区全景图" />
  </div>

  <div class="image-container">
    <img src="/images/disaster/disaster5-4.png" alt="道路损毁情况" />
  </div>

  <div class="image-container">
    <img src="/images/disaster/disaster5-5.png" alt="房屋受损分析" />
  </div>
`);
</script>

<style scoped>
.page-container {
  background-color: #f5f7fa;
  min-height: 100vh;
}

/* 如果需要图片并排显示，可以添加这个样式到template.vue中 */
:deep(.image-row) {
  display: flex;
  gap: 20px;
  margin: 20px 0;
}

:deep(.image-row .image-container) {
  flex: 1;
  min-width: 0;
}
</style>